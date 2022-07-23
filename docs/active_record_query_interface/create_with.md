# create_with

- sets attributes to be used when creating new records from a relation object

## usages

find male users, if it doesn't exist, create male user with name of HogeHoge
```
User.create_with(name: 'HogeHoge').find_or_create_by(sex: 'male')
```

refs:
https://qiita.com/pekepek/items/c57d4859e6e1ec8b1ad1

https://api.rubyonrails.org/v7.0/classes/ActiveRecord/QueryMethods.html#method-i-create_with
