#### Requirements

You'll need the following installed to run the template successfully:

* Ruby 3.1.2
* bundler - `gem install bundler`
* PostgreSQL - `brew install postgresql`

#### Initial Setup
* Install other gems using bundler

    ```
    bundle install
   ```
* Start postgres server

    ```
    brew services start postgresql
    ```    
* Create database

    ```
    rails db:create
    ```    
* Migrate the database
    ```
    rails db:migrate
    ```

#### Running application

```bash
rails server
```

