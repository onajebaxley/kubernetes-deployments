## onaje.baxley@analog.com 1/7/19
## Defines Docker image to be run by cluster's Jenkins executors

# Start from standard chart-slave image
FROM jenkins/jnlp-slave:3.10-1

# Install nvm and output/verify version
apt-get update
apt-get install build-essential libssl-dev
curl https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
source ~/.profile
nvm --version

