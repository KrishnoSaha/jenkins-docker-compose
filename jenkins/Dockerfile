FROM jenkins/jenkins:lts-jdk17

# docker cli only, the daemon runs in the dind container
COPY --from=docker:27-cli /usr/local/bin/docker /usr/local/bin/docker

# plugins the pipeline needs
RUN jenkins-plugin-cli --plugins \
    workflow-aggregator git docker-workflow credentials-binding \
    audit-trail matrix-auth timestamper build-timeout
