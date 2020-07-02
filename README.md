# Python Django API Reference Project

This is reference project which "dockerised" a Python Django API app, and creates a CI/CI pipeline on TravisCI

## Build/Run Locally

To build the Docker image , run the following command:

```bash
docker-compose up --build
```

To run the app locally , run the following command:

```bash
docker-compose up # app starts at http://localhost:8000/
```

In a seperate terminal window, create a new Django superuser by running the following command:

```bash
docker-compose run app sh -c "python manage.py createsuperuser" # follow instructions to create a new Django superuser
```

## Usage

- To run tests, run the following command:

```bash
docker-compose run app sh -c "python manage.py test && flake8"
```

- To create a new user, once the app is running visit `http://localhost:8000/api/user/create/`

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
