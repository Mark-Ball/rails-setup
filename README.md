# How to set up a rails project with Postgres

## 1. Create rails project

```rails new projectname -d=postgresql```

## 2. Start postgres locally

```sudo service postgresql start```

Then confirm it is working

```sudo -u posgres psql```

## 3. Create the database

```rails db:create```

## 4. Generate and perform migrations

Basic migration to create a table

```rails generate migration CreateProducts name:string```

```rails db:migrate```

## 5. Connect dbeaver

- New database connection
- Database: get name from line 26, config/database.yml of rails project e.g. my_project_development
- Enter your user and password
- Test connection => finish

## 6. Test it all works

We can now create an entry in the products table using the rails console and see it appear in dbeaver.

```rails c```
```Product.create({name: 'toy'})```