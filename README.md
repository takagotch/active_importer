### active_importer
---
https://github.com/continuum/active_importer

```sh
gem 'active_importer'
bundle
gem install active_importer

```

```ruby
class EmployeeImporter < ActiveImporter::Base
  imports Employee
  column 'First name',  :first_name
  column 'Last name', :last_name
  column 'Department', :department do |department_name|
    Department.find_by(name: department_name)
  end
end

EmployeeImporter.import('/path/to/file.xls')


```
https://github.com/continuum/active_importer/wiki


```
```


