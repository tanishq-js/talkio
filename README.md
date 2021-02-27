## Setup instructions (tested on macOS 10.15 Catalina)

First install the dependencies:

1. Clone the repository.
2. `cd` into the directory and run `npm install`.
3. Run `cd client && npm install`.

Next, set up the database credentials:

1. Log into or create an [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account.
2. Create a new MongoDB cluster. You can go with the default settings or customize them as you wish. Once the cluster is created, click "Connect."
   ![Create Cluster](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/createCluster.png)
   ![Connect](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/connect.png)
3. Whitelist a connection IP address and create a new MongoDB user.
   ![Setup Security](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/setupSecurity.png)
4. Once connection security is set up, choose "Connect Your Application."
   ![Connect Application](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/connectApplication.png)
5. Replace the dbURI in `secrets.js`, located in backend folder, with the connection string. Replace `someUser` and `<password>` with the user and password you created in step 2.
   ![Connection String](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/connectionString.png)
   ![Sample Secrets](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/sampleSecrets.png)
6. `cd` back into the main directory and run `npm start`. You can access the site at `localhost:3000`.

Optional: If you want to also deploy the app to Heroku, first go through the aforementioned steps and then proceed as follows:

1. Log into or create a [Heroku](https://heroku.com/) account.
2. Create a new app in Heroku.
   ![Create New App](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/createNewApp.png)
3. In the settings tab, add the config vars for REACT_APP_DB_URI and REACT_APP_JWT_KEY. The value for REACT_APP_DB_URI should be the same as the one you previously entered for dbURI in `secrets.js`. REACT_APP_JWT_KEY can be set to any random string.
   ![Heroku Config Variables](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/herokuConfigVars.png)
4. In the deploy tab, choose any deployment method to deploy the application.
   ![Deploy Heroku](https://github.com/jm-shi/MERN-Social-Network/blob/master/demo/deployHeroku.png)

## Built With

- [Express.js](https://expressjs.com/) - Backend web framework
- [Heroku](http://heroku.com/) - Platform to deploy web applications
- [JSON Web Token](https://jwt.io/) - A standard to securely authenticate HTTP requests
- [Material-UI](https://material-ui.com/) - UI library for React
- [MongoDB](https://www.mongodb.com/) - Database to store document-based data
- [Mongoose](https://mongoosejs.com/) - Object-modeling tool for Node.js
- [Node.js](https://nodejs.org/en/) - Runtime environment to help build fast server applications
- [React](https://reactjs.org/) - JavaScript library for building user interfaces
- [Redux](https://redux.js.org/) - JavaScript library to help better manage application state

