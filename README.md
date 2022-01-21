# repo
for this website you will also need:
-enterprisedb
-initialise npm for js and install libaries 

to initialise npm you will need to instal your prefered js compiler and follow online instructions acordingly 
after you initialise npm you will need to install libaries
you can do it with just one command
-npm i express.js body-parser knex pg nodemon

after you finish installing npm libaries you should be able to open your website in your localhost acordingly to the server.js file
if you want to be able to open your website on another device for free, you can set-up ngrok
after you install ngrok, you can initialise hosting with command ngrok.exe (your ip from server.js - by default 127.0.0.1):(your port from server.js by default 3000)

after you done all of that, you will be able to connect to the website and iteract with it, but the login and register wont work/will crash the site
its becouse you dont have a database 
// for windows
to create a database you will need to install enterprisedb // while installing make sure you remember the password
after you install enterprisedb you will need to change the password in server.js file to the enterprisedb password you created while installing
after you done all that you can set up the database with following commands:
in pgAdmin:
CREATE TABLE users (
	user_id serial PRIMARY KEY,
	name VARCHAR ( 50 ) UNIQUE NOT NULL,
	password VARCHAR ( 50 ) NOT NULL,
	email VARCHAR ( 255 ) UNIQUE NOT NULL
);

in sql_shell:
sql>create database
posgresql > properties > connection > hostname/adress :127.0.0.1(the adress in server.js)
home>querytool> (imput code from pgadmin after creating the table)

if you done all of the steps you should have a running website with all the features working
