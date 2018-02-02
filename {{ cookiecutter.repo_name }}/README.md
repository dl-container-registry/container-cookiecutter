# {{cookiecutter.project_name}}

[![Build Status](https://travis-ci.org/{{cookiecutter.github_username}}/{{cookiecutter.repo_name}}.svg)](https://travis-ci.org/{{cookiecutter.github_username}}/{{cookiecutter.repo_name}})
[![Dockerhub link](https://img.shields.io/badge/hosted-dockerhub-22b8eb.svg)](https://hub.docker.com/r/{{cookiecutter.dockerhub_username}}/{{cookiecutter.image_name}}/)
[![Singularity hub link](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/{{cookiecutter.singularityhub_id}}) 

{{ cookiecutter.description }}

## Usage


### Docker

```bash
$ docker run --rm {{cookiecutter.dockerhub_username}}/{{cookiecutter.image_name}}
```


### Singularity

Run a shell session in the container

```bash
$ singularity shell shub://{{cookiecutter.github_username}}/{{cookiecutter.repo_name}}
```

Run a program named `<program>` in the container.

```bash
$ singularity exec
shub://{{cookiecutter.github_username}}/{{cookiecutter.repo_name}} <program> ```
t
