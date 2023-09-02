FROM ghcr.io/rocker-org/devcontainer/tidyverse:4

# see: https://stackoverflow.com/a/49676568
# Update default packages
RUN apt-get update

# Get Ubuntu packages
RUN apt-get install -y \
    build-essential \
    curl

# Update new packages
RUN apt-get update

# Get Rust
RUN curl https://sh.rustup.rs -sSf | bash -s -- -y

# set path
ENV PATH="/root/.cargo/bin:${PATH}"

# R: install additional r-packages
RUN R -q -e 'install.packages(c("rextendr"))'

