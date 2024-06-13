### Clone the repo locally

`git clone https://github.com/aarthi-mallow/contacts-crud.git`

### Requirements

You'll need the following installed to run the application successfully:

* Ruby 3.1.2
* bundler - `gem install bundler`
* PostgreSQL - `brew install postgresql`

### Initial Setup
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

### Running application
To start the application in development mode run the below,
```bash
rails server
```

Open your web browser and navigate to `http://localhost:3000` to view the application.


## Architectural Decisions

- **Scaffolding**: Used Rails scaffold generator to quickly set up the CRUD functionality, ensuring rapid development.
- **Validations**: Added basic validations in the model to ensure data integrity.
- **Administrate gem**: Added Administrate gem for quickly building UI for the CRUD. For non-admin pages, we can consider going with boostrap or rails templates for quickly building application.

## Scalability

- **Pagination**: Pagination should be added for all the list pages. Since it came with administrate, I didn't add paginate separately for contacts CRUD
- **Background Jobs**: We should use background tasks for long processes like sending many emails at once
- **Load Balancing**: Distribute traffic across multiple servers to handle more users and ensure the app is always available.
- **RAILS thread count**: We can increase rails thread count as needed(once the app grows) to serve more requests concurrently.

## Maintainability
- **Automtated Test cases**: Maintaining automated test cases for each feature will help us to catch bugs early and ensure the app works as expected. This makes future changes safer. 
- **Update Dependencies**: Regularly update the tools and libraries the app uses to keep it secure and efficient.

