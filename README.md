# splat! login

## Description
loginpagebark is a Node.js web application for user authentication, featuring a login and registration system. It uses Express.js for handling web routes and API, MySQL for database interactions, and JWT for session management. The server-side HTML rendering is managed with hbs (Handlebars), and user passwords are secured using bcryptjs.

## Prerequisites
Before you begin, ensure you have met the following requirements:
* You have a basic understanding of JavaScript and Node.js.
* You have Node.js and npm installed. See [Node.js](https://nodejs.org/) for installation instructions.
* You have MySQL installed and running on your server. See [MySQL](https://dev.mysql.com/doc/mysql-installation-excerpt/5.7/en/) for installation instructions.

## Technologies Used
- **Express.js**: For creating API and web routes and setting up the app backend.
- **MySQL**: For connecting to the MySQL server.
- **dotenv**: For managing environmental variables securely.
- **hbs**: For rendering HTML on the server.
- **Bcryptjs**: For hashing passwords.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/cre8ture/nodeJS-login.git
    cd loginpagebark
    ```

2. Install NPM packages, including nodemon for development convenience:
    ```bash
    npm install
    npm i nodemon --save
    ```

3. In your `package.json` file, under scripts, add the start script:
    ```json
    "scripts": {
      "start": "nodemon app.js"
    }
    ```

4. Create a `.env` file in the root directory of the project and update it with your database configuration and JWT settings:
    ```plaintext
    DATABASE=login_db
    DATABASE_HOST=localhost
    DATABASE_USER=<your db user>
    DATABASE_PASSWORD=<your db password>
    JWT_SECRET=<your jwt secret>
    JWT_EXPIRES_IN=3600  # Expires in 1 hour
    JWT_COOKIE_EXPIRES=90 # Cookie expires in 90 days
    ```

## Setting Up the Database
1. Create a new database in your MySQL environment named `login_db`.
2. Build a users table with the following schema:
   - ID: INT, AUTOINCREMENT
   - Name: VARCHAR
   - Email: VARCHAR
   - Password: VARCHAR
3. Ensure your database schema matches the expected structure for the application.

## Running in Production
1. Ensure all environment variables are set correctly in the `.env` file.
2. Start the application using the start script:
    ```bash
    npm start
    ```
3. Your application should now be running on the defined port.

## Contributing to splat! login
<!-- Contribution guidelines -->
- please use this as you please
- your suggestions are welcome. Make a pull request or message me at bakukai@gmail.com

## License
This project uses the following license: [MIT](https://opensource.org/licenses/MIT).
