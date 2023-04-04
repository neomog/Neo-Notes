# NEONOTES

## Guide to Setup on your environment
1. Clone this repository into your local machine using the terminal (Mac), CMD (Windows), or a GUI tool like SourceTree.
2. Navigate into your project directory
    ```
    cd <your-project-name>
    ```
3. Install project dependencies using the following command:
    ```
    composer install --ignore-platform-reqs
    ```
4. Create the .env file from the example file
    ```
    cp .env.example .env
    ```
5. Open the .env file and change the database configuration to the following
    ```
    DB_CONNECTION=mysql
    DB_HOST=mysql
    DB_PORT=3306
    DB_DATABASE=<your-project-name>
    DB_USERNAME=sail
    DB_PASSWORD=password
    ```
   
   - Or preferably use the existing sqlite DB by modifyin the above to the following
    ```
        DB_CONNECTION=sqlite
    ```
   - Then create an sqlite file as is already created using the following command
   ```
        touch database/database.sqlite
   ```

6. Start Project with the command
    ```
    php artisan serve
    ```
    Leave this command running.
7. Open a new terminal tab to generate application key
    ```
    php artisan key:generate
    ```
8. Migrate database tables
    ```
    php artisan migrate
    ```
9. Go to localhost on your browser to view the application

