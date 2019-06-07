Workarea Sandbox
================================================================================

Get a sandbox instance of Workarea running with Docker.

Setup
--------------------------------------------------------------------------------

To get setup a sandbox application, clone this repository, navigate to its directory, and run the setup command.

```bash
git clone https://github.com/workarea-commerce/workarea-sandbox.git
cd workarea-sandbox
bin/setup
```

The setup script will build the application image, start the Docker containers, and run the application seeds provided by Workarea. Once setup has finished, you can navigate to `http://localhost:3000` to see your application.

To stop the application, run:

```bash
docker-compose down
```

If you want to restart an existing sandbox, run:

```bash
docker-compose up
```

Using the `bin/setup` script will cause the application image to rebuild and the application to reseed, which will result in a longer load time than necessary for existing application.

Troubleshooting
--------------------------------------------------------------------------------

If any of the Docker containers fail to start make sure you do not have any other services or containers running that are using the same ports.

Workarea services use ports `27018`, `9201`, `6389`, and `3000`.
