# annotate
- Rails 6 adds ActiveRecord::Relation#annotate
- purpose: to write SQL comment to queries
- allows to use multiple annotations
- allows annotation scopes & modal associations

## usages
 
```
User.annotate('selecting user names').select(:name)
```
> SELECT "users"."name" FROM "users" /* selecting user names */

```
bigbinary = Organization.find_by!(name: "BigBinary")

User.annotate("User whose name starts with 'A'")
    .annotate("AND belongs to BigBinary organization")
    .where("name LIKE ?", "A%")
    .where(organization: bigbinary)
```

```
scope :active, -> { where(status: 'active').annotate("Active users") }
```

refs:
https://api.rubyonrails.org/classes/ActiveRecord/QueryMethods.html#method-i-annotate

https://www.bigbinary.com/blog/rails-6-adds-annotate-to-activerecord-relation-queries
