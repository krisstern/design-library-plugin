FROM gitpod/workspace-full

USER gitpod

ARG NODE_VERSION=20.18.1

# Install Java 21.0.4-tem and Node.js v20.18.1
RUN brew install gh && \
    bash -c ". /home/gitpod/.sdkman/bin/sdkman-init.sh && \
    sdk install java 21.0.4-tem && \
    sdk default java 21.0.4-tem" && \
    bash -c "source $HOME/.nvm/nvm.sh && nvm install $NODE_VERSION \
    && nvm use $NODE_VERSION && nvm alias default $NODE_VERSION"

# Ensure nvm uses the default version on every new terminal session
RUN echo "nvm use default &>/dev/null" >> ~/.bashrc.d/51-nvm-fix
