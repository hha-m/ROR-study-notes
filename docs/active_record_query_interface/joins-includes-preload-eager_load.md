# includes, preload, eager_load
- to solve Active Record N+1 query problem

Q1. load association records in
(i) single query by joining tables
(ii) seperate queries

Q2. able to query on
(i)first table
(ii)second table

| |  Q1 |Q2|merit| demerit
|-----|-----|:----:|:----:|:----:|
| preload | (ii) | (ii) |higher speed than eager_load||
| eager_load | (i) with left outer join| (ii) | | takes too many response time|
| includes | (ii)| (ii) | ||

## preload

### Usages
```
User.preload(:posts).to_a

# =>
SELECT "users".* FROM "users"
SELECT "posts".* FROM "posts"  WHERE "posts"."user_id" IN (1,..,100)
```

### Conditions
```
User.preload(:posts).where("users.name='HogeHoge'")

# =>
SELECT "users".* FROM "users"  WHERE (users.name='HogeHoge')
SELECT "posts".* FROM "posts"  WHERE "posts"."user_id" IN (3)
```

```
User.preload(:posts).where("posts.desc='ruby is awesome'")

<Exception>
```

## eager_load

### Usages
```
User.eager_load(:posts).to_a

# =>
SELECT "users"."id" AS t0_r0, "users"."name" AS t0_r1, "posts"."id" AS t1_r0,
       "posts"."title" AS t1_r1, "posts"."user_id" AS t1_r2, "posts"."desc" AS t1_r3
FROM "users" LEFT OUTER JOIN "posts" ON "posts"."user_id" = "users"."id"
```

### Conditions
```
User.preload(:posts).where("posts.article like ?","%active record%")

# =>
SELECT "users"."id" AS t0_r0, "users"."name" AS t0_r1, "posts"."id" AS t1_r0,
       "posts"."title" AS t1_r1, "posts"."user_id" AS t1_r2, "posts"."desc" AS t1_r3
FROM "users" LEFT OUTER JOIN "posts" ON "posts"."user_id" = "users"."id"
WHERE (posts.article like "%active record%")
```

## includes

### Usages
```
users = User.includes(:address)
users.each do |user|
  user.address.city
end
```

```
users = User.includes(:address, :friends)
```

```
users = User.includes(:address, friends: [:address, :followers])
```

### Conditions
```
User.includes(:posts).where('posts.name = ?', 'example').references(:posts)

User.includes(:posts).references(:posts).where('posts.name = ?', 'example')

User.includes(:posts).where(posts: { name: 'example' })
```

```
User.includes(:posts).where('posts.name = ?', 'example')

<exception>
```

refs:
https://qiita.com/south37/items/b2c81932756d2cd84d7d
