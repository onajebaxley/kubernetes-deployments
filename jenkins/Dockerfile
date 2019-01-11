## onaje.baxley@analog.com 1/7/19
## Defines Docker image to be run by cluster's Jenkins executors

# Start from standard chart-slave image
FROM jenkins/jnlp-slave:3.10-1
ARG NODE_VERSION=8

# Install node/npm and output/verify version
USER root
ENV NODE_VERSION=${NODE_VERSION}

RUN apt-get update
RUN apt-get install -y build-essential libssl-dev
RUN curl -sL "https://deb.nodesource.com/setup_$NODE_VERSION.x" | bash -
RUN apt-get install -y nodejs

# Return to nonprivileged user
USER jenkins
RUN node --version

# Default entrypoint is jenkins-slave binary
ENTRYPOINT ["jenkins-slave"]

