# lynx-runner

- [lynx-runner](#lynx-runner)
  - [Architecture](#architecture)
  - [Development](#development)
      - [version 0.1:](#version-01)

Runner is a microservice handling code execution requests.

## Architecture

The idea is to make the service both safe and easy to tune to various needs,
so we'd like to dispatch user code into docker containers and run it in a
safe and consistent environment. Also, we want to keep it as simple as possible.

## Running in container
In order to run `lynx-runner:0.4` with `lynx-runtime:0.3` at port `9233` use:

    podman pull ghcr.io/group-project-gut/lynx-runner:0.4
    podman run --privileged -p 9233:9233 lynx-runner:0.4 0.3 9233

## Development

#### version 0.1:

- [X] reading JSON input from front-end
- [X] running user code in podman container
