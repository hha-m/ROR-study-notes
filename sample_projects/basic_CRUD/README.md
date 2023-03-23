# README

- Ruby version
`3.0.3`

- Rails version
`7.0.4.3`

- Database
`sqlite`

## procedures

1. Create project
```
rails new basic_CRUD
```

2. Start the server: To start the Rails server, navigate into the basic_CRUD directory and run the following command in your terminal
```
rails server
```

then, before next step, quit from server with Ctrl + C

3. Create CRUD: To create a CRUD (Create, Read, Update, Delete)
Rails provides a built-in generator for creating a scaffold, which is a quick way to generate a full set of CRUD actions for a resource.
To generate a scaffold for a resource called Post, run the following command in your terminal:
```
rails generate scaffold Post title:string body:text
```

4. Run the migration to create the posts table in the database
```
rails db:migrate
```

5. Start the server again
```
rails server
```

6. Navigate to the index page: Open your web browser and navigate to 
http://localhost:3000/posts