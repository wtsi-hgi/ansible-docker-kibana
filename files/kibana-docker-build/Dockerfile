FROM docker.elastic.co/kibana/kibana-oss:6.2.4

ENV KIBANA_INSTALL_DIRECTORY=/usr/share/kibana
ENV STEAM_GUARD_VERSION=6.2.4-13

RUN curl https://search.maven.org/remotecontent?filepath=com/floragunn/search-guard-kibana-plugin/${STEAM_GUARD_VERSION}/search-guard-kibana-plugin-${STEAM_GUARD_VERSION}.zip > /tmp/search-guard-kibana-plugin.zip \
    && "${KIBANA_INSTALL_DIRECTORY}/bin/kibana-plugin" install file:///tmp/search-guard-kibana-plugin.zip \
    && rm /tmp/search-guard-kibana-plugin.zip

