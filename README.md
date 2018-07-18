# Ants (Because ants are good in carrying items from different places)
Managing Customer Order Shipments

Libraries used:
React, Webpack, SASS

Platform:
NODE, NPM

Running App (Demo):  (It will be slow the first time)

Steps to install and run locally:

    git clone https://github.com/vikaskulkarni/Ants.git
    cd Ants
    npm install

    cd Ants/client
    npm install
    npm run build
  
The above step will create a dist folder. index.html can be run in any web server.
Install http-server globally

To Start Client
    npm i -g http-server
    cd Ants/client/dist
    http-server -p 65132
To Start Server
    cd Ants
    npm run start-server
  
Navigate to http://localhost:65132/. In this mode, the code changes are NOT automatically loaded. Make sure the underlying service layer is running on 3001 that serves the APIs
  
Development Mode

    cd Ants
    npm run start-dev
  
Navigate to http://localhost:65132/. In this mode, the code changes are automatically loaded. Make sure the underlying service layer is running on 3001 that serves the APIs


Looking at the project structure:

Client (Ants/client)
    components

        This contains the reusable components like header, footer, table, search. These are standalone components that can be used by any pages by passing required props.

    containers

        This contains the Application container, App.jsx that embeds all the required components to design the page. The application has;
        - header
        - table to list the Ad slots
        - form to show the Ad details and create, edit

    service

        This is common api layer that uses 'axios' library to make server calls

Server (Ants/server)
    server.js

        This is the main entry point for the server code and contains all the REST end points required by the client
        
    entities

        This contains the schemas for handling mongodb models