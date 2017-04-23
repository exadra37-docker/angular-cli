FROM exadra37/node-zsh:latest

LABEL "com.exadra37.vendor"="Exadra37"
LABEL com.exadra37.package-name="exadra37-docker-images/angular-cli"
LABEL description="Angular CLI image build from exadra37/node-zsh that build on top of the official Node image."

ARG ANGULAR_CLI_TAG="${ANGULAR_CLI_TAG:-1.0.0}"
ARG NODE_EXPOSE_PORT="${NODE_EXPOSE_PORT:-4200}"

# The official image as a user called "node" that as the UID 1000.
# Once the UID 1000 normally will match the one used in our OS, than we will avoid permissions issues when mapping
#  volumes between the host and container.
ARG CONTAINER_USER="node"

WORKDIR /home/"${CONTAINER_USER}"/workspace

RUN npm install -g @angular/cli@"${ANGULAR_CLI_TAG}" && \
    npm cache clean

EXPOSE "${NODE_EXPOSE_PORT}"

CMD ["zsh"]
