# BLG317E-Project
## Introduction

This is our group project for BLG317E class. In the project, we are supposed to use a dataset and create a website from it. The website is supposed to have CRUD functionality, and extra features can be added if we want. The data that we used was from this [repo](https://github.com/jfjelstul/worldcup). For the frontend, we used JavaScript and the React library, which was optional. As for the backend, we used Python and Flask, which was mandatory for the course.

## Setup

To setup the project first create the docker images using makefile. There are 2 necessary docker images need to be running for the application to work: mysql and frontend. To build and start these images follow instructions below:

```
make mysql
make frontend-build
```

In order for the database to work it needs to have the tables inside it. In order to create the database run the following command
```
make createdb
docker exec -it fifa-mysql mysql -u root --password=root
```

After these instructions you will be in the mysql interface. Then we need to copy all the data inside data.sql. So select fifa database and paste the data.sql inside mysql. After these operations the mysql server should be ready.

Then to start the servers and see the page run the following make instruction:

```
make start-servers
```

## Main Features

The main features of the project include:

- Live showcasing of CRUD operations on various tables through updating the frontend and the backend.
- Sorting and filtering capabilities.
- Implementation of scroll pagination.
- Implementation of a Smart search bar.
- Validation of inputs.
- Statistical calculations.
