# gitlab-runner-compose

# GitLab Runner with Docker Compose

This project demonstrates how to setup a GitLab Runner using Docker Compose.
It aims to provide a simple and easy to use Docker based solution for self hosting
a GitLab CI/CD runner using Docker containers without running as root. 
It also enables jobs to be run in isolation by starting a new podman rootless docker API
for every new runner.

It makes heavy usage of podman running rootless inside containers to make a
docker compatible API available to the gitlab-runner container.

# Usage #
Get a gitlab runner token and start the compose.yml with
`GITLAB_REGISTRATION_TOKEN=... docker-compose up`

At this point you can also scale the number of available
runners with `GITLAB_REGISTRATION_TOKEN=... docker-compose scale executor=5`

# TODO #
- kill the gitlab single-run runner after every job