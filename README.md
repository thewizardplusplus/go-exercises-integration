# go-exercises-integration

Integration of the background worker, back-end, and front-end of the service for solving programming exercises.

## Components

- [go-exercises-worker](https://github.com/thewizardplusplus/go-exercises-worker) v1.1.6;
- [go-exercises-backend](https://github.com/thewizardplusplus/go-exercises-backend) v1.7.2;
- [go-exercises-frontend](https://github.com/thewizardplusplus/go-exercises-frontend) v1.5.2.

## Workflow

### Cloning

This repository contains submodules. Therefore, clone it as follows:

```
$ git clone --recurse-submodules https://github.com/thewizardplusplus/go-exercises-integration.git
$ cd go-exercises-integration
```

### Pulling

To pull updates, run the following commands:

```
$ git pull --recurse-submodules
$ git submodule update --recursive --init
```

## Migration

The necessary tables will be created automatically on service starting.

Then run the manual migration to create a few example tasks (optionally):

```
$ ./go-exercises-backend/tools/migrate.sh -h | --help
$ ./go-exercises-backend/tools/migrate.sh
```

Options:

- `-h`, `--help` &mdash; show the help message and exit.

Environment variables:

- `PATH_TO_MIGRATIONS` &mdash; path to migrations (default: `./go-exercises-backend/migrations`);
- `STORAGE_ADDRESS` &mdash; [PostgreSQL](https://www.postgresql.org/) connection URI (default: `postgres://postgres:postgres@localhost:5432/postgres?sslmode=disable`).

## License

The MIT License (MIT)

Copyright &copy; 2021-2022 thewizardplusplus
