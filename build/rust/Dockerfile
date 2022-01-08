FROM rust:1.57-slim-bullseye

ARG UID 1000
ARG GID 1000

ENV UID=$UID
ENV GID=$GID

RUN echo "UID=${UID}; GID=${GID}"
RUN apt update; apt upgrade; apt install -y zsh git curl
RUN groupadd --gid $GID rustuser; useradd --uid $UID --gid $GID -ms /usr/bin/zsh rustuser; mkdir /home/rustuser/projects

USER $UID:$GID

WORKDIR /home/rustuser/projects
VOLUME /home/rustuser/projects

ENTRYPOINT ["tail", "-F", "something_non_existant"]