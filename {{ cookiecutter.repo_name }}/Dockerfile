FROM nvidia/cuda:8.0-devel-ubuntu16.04 as build
LABEL maintainer="{{ cookiecutter.email_address }}"

RUN apt-get update && apt-get install -y \
        wget

FROM nvidia/cuda:8.0-runtime-ubuntu16.04
RUN apt-get update && apt-get install -y \
        wget \
    && rm -rf /var/cache/apt
COPY --from=build /install/* /usr/local/lib/

ENV NVIDIA_VISIBLE_DEVICES all
ENV NVIDIA_DRIVER_CAPABILITIES video,compute,utility

VOLUME /workspace
WORKDIR /workspace
ENTRYPOINT ["/path/to/executable"]
CMD ["--help"]
