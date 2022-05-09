FROM gitpod/workspace-java-11:2022-05-08-14-31-53

RUN bash -c ". /home/gitpod/.sdkman/bin/sdkman-init.sh && \
    sdk use java 11.0.9.j9-adpt && \
    yes | sdk install jbang && \
    rm -rf $HOME/.sdkman/archives/* && \
    rm -rf $HOME/.sdkman/tmp/* "

# install jbang 
RUN bash -c '$HOME/.sdkman/candidates/jbang/current/bin/jbang --version'

RUN bash -c '$HOME/.sdkman/candidates/jbang/current/bin/jbang trust add https://repo1.maven.org/maven2/io/quarkus/quarkus-cli/'

# install quarkus cli
RUN bash -c '$HOME/.sdkman/candidates/jbang/current/bin/jbang app install --fresh --force quarkus@quarkusio'
