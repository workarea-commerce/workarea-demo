Workarea Demo
================================================================================

Get a demo instance of Workarea running with Docker.

Setup
--------------------------------------------------------------------------------

To get setup a demo application, you can run the follow command:

```bash
curl -s https://raw.githubusercontent.com/workarea-commerce/workarea-demo/master/bin/install | bash
```

This will run a script that does the following:

* clone this repository.
* build a Docker image for the application
* start containers for the application and required services
* seed the database
* start the application server

If you have already cloned this repository, you can simply run:

```bash
bin/setup
```

Once complete, you can visit `http://localhost:3000` to view your app. The seed data provides an admin user with an email/password of `user@workarea.com/w0rkArea!`.

To stop the application, run:

```bash
docker-compose down
```

If you want to restart an existing demo app, navigate to the `workarea-demo/` directory and run:

```bash
docker-compose up
```

Using the `bin/setup` script will cause the application image to rebuild and the application to reseed, which will result in a longer load time than necessary for an existing application.

Troubleshooting
--------------------------------------------------------------------------------

If any of the Docker containers fail to start make sure you do not have any other services or containers running that are using the same ports.

Workarea services use ports `27018`, `9201`, `6389`, and `3000`.
