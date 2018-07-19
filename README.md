# Ants (Because ants are good in carrying items from different places)
Managing Customer Order Shipments

Libraries used:
React, Webpack, SASS

Platform:
NODE v8.6.0, NPM v5.3.0

Running App (Demo): http://ec2-184-73-148-247.compute-1.amazonaws.com:3001/ (It will be a bit slow the first time)

Steps to install and run locally:

    git clone https://github.com/vikaskulkarni/Ants.git
    cd Ants
    npm install

    cd Ants/client
    npm install
  
Production Mode
    
    cd Ants/client
    npm run build
    cd Ants
    npm run start-server

Navigate to http://localhost:3001/. Here node server is serving the client files as well.

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
        
For Database, Mongo is used as a service through https://www.mlab.com/

Wiki for REST end points:
https://github.com/vikaskulkarni/Ants/wiki/REST-End-Points-for-Order,-Customer-and-Product-Management
