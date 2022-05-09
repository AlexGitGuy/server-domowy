to install libaries:
-npm i express.js body-parser knex pg nodemon

to create sql table(for login and password database) use command:
CREATE TABLE users (
	user_id serial PRIMARY KEY,
	name VARCHAR ( 50 ) UNIQUE NOT NULL,
	password VARCHAR ( 50 ) NOT NULL,
	email VARCHAR ( 255 ) UNIQUE NOT NULL
);


