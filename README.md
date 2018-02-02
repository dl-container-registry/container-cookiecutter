# HPC Container CookieCutter

Container template repo for building joint docker and singularity images. The
template assumes the docker image contains the container, and the singularity
file simply pulls down the docker image and converts it to a singularity
container.

## Installation


## Usage

* Instantiate template using `cookiecutter`:
  `cookiecutter https://github.com/dl-container-registry/container-cookiecutter`
* Create a [new github repository](https://github.com/new) with the same name
  that you entered for `repo_name` in the template.
* Set up GitHub Auto-Deployment integration in settings.
  * Github Token: Your GitHub token (obtained from [developer
    settings](https://github.com/settings/tokens) with `repo_deployment` privileges)
  * Environment: `singularity`
  * Deploy on status: tick
  * GitHub api url: empty

* Set up Singularity hub
  * Create a [new container collection](https://www.singularity-hub.org/collections/new).
  * Change settings:
    * Build Trigger: Deployment
  * Save.
  * Note Singularity Hub ID, replace `SH_ID` with your ID in the README.

* Set up [Travis](https://travis-ci.org/)
  * [Enable travis on repository](https://travis-ci.org/profile/).
  * Click the cog next to the repository to go to the settings.
  * Set `DOCKER_USERNAME` to your docker username.
  * Set `DOCKER_PASSWORD` to your docker password (make sure you to quote the full
    password in case your password has special characters).
