.PHONY: build push singularity clean
SHELL:=bash
CONTAINER_NAME:={{cookiecutter.dockerhub_username}}/{{cookiecutter.image_name}}
SINGULARITY_IMAGE:={{cookiecutter.image_name}}.simg


build:
	docker build -t $(CONTAINER_NAME) .

push:
	docker push $(CONTAINER_NAME)

singularity: $(SINGULARITY_IMAGE)

$(SINGULARITY_IMAGE):
	singularity build $@ Singularity

clean:
	rm $(SINGULARITY_IMAGE)
