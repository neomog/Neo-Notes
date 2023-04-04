# NEONOTES

Learn about MVC architecture, how the Laravel framework is structured, routes and controllers, Blade files, models, and best practices for interacting with a database. Get tips on using various components in Laravel as you build your own simple note-taking app. From user authentication and routing, to CRUD operations and database relations, find out why the latest version, Laravel 9.0, allows you to build web apps quickly and easily, no matter where you are on your coding journey.

## Instructions
This repository has branches for each of the videos in the course. You can use the branch pop up menu in github to switch to a specific branch and take a look at the course at that stage, or you can add `/tree/BRANCH_NAME` to the URL to go to the branch you want to access.

## Branches
The branches are structured to correspond to the videos in the course. The naming convention is `CHAPTER#_MOVIE#`. As an example, the branch named `02_03` corresponds to the second chapter and the third video in that chapter. 
Some branches will have a beginning and an end state. These are marked with the letters `b` for "beginning" and `e` for "end". The `b` branch contains the code as it is at the beginning of the movie. The `e` branch contains the code as it is at the end of the movie. The `main` branch holds the final state of the code when in the course.

When switching from one exercise files branch to the next after making changes to the files, you may get a message like this:

    error: Your local changes to the following files would be overwritten by checkout:        [files]
    Please commit your changes or stash them before you switch branches.
    Aborting

To resolve this issue:
	
    Add changes to git using this command: git add .
	Commit changes using this command: git commit -m "some message"

## Setup on your environment
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

