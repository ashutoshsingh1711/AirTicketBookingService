# BOOKING MICROSERVICE

## INSTALL DEPENDENCIES

    npm i express;
    npm i body-parser;
    npm i http-status-codes;
    npm i mysql2;
    npm i sequelize sequelize-cli;
    npm i nodemon;
    npm i dotenv;
    npm i morgan;

## SETUP SEQUELIZE

    npx sequelize init; // CREATE FOLDERS
    npx sequelize db:create  // CREATE DATABASE ON MYSQL

    npx sequelize model:generate --name Booking --attributes flightId:integer,userId:integer,status:ENUM
    npx sequelize db:migrate

    //Update model Booking
    npx sequelize migration:create --name modify_bookings_add_new_fields
    npx sequelize db:migrate

    <!-- JFK - npx sequelize db:migrate:undo is used to revert the last migration -->
