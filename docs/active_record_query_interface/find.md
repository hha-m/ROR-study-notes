# find
- one of the finder methods
- fetch single or multi records from table

## usages

```
Person.find(1)          # returns the object for ID = 1
Person.find("1")        # returns the object for ID = 1
Person.find("31-sarah") # returns the object for ID = 31

Person.find(1, 2, 6)    # returns an array for objects with IDs in (1, 2, 6)
Person.find([7, 17])    # returns an array for objects with IDs in (7, 17)
Person.find([1])        # returns an array for the object with ID = 1
Person.where("administrator = 1").order("created_on DESC").find(1)
```

## variations of find

### find_by
```
# If no record is found, returns nil
Person.find_by(name: 'Spartacus')

# If no record is found, raises an ActiveRecord::RecordNotFound error exception
Person.find_by!(name: 'Spartacus')
```

others
```
Person.find_or_initialize_by(name: 'Spartacus', rating: 4)

Person.find_or_create_by(name: 'Spartacus', rating: 4)

```

[exists?](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-exists-3F)

[fifth](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-fifth), [fifth!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-fifth-21), [find](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-find), [find_by](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-find_by), [find_by!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-find_by-21), [find_sole_by](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-find_sole_by), [first](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-first), [first!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-first-21), [forty_two](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-forty_two), [forty_two!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-forty_two-21), [fourth](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-fourth), [fourth!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-fourth-21)

[include?](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-include-3F)

[last](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-last), [last!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-last-21)

[member?](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-member-3F)

[second](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-second), [second!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-second-21), [second_to_last](), [second_to_last!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-second_to_last), [sole](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-sole)

[take](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-take), [take!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-take-21), [third](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-third), [third!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-third-21), [third_to_last](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-third_to_last), [third_to_last!](https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html#method-i-third_to_last-21)

refs:
https://api.rubyonrails.org/v7.0.3/classes/ActiveRecord/FinderMethods.html