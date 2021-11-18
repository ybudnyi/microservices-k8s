FROM java:8
ARG JMETER_VERSION="5.3"

RUN cd /opt \
 && wget https://downloads.apache.org//jmeter/binaries/apache-jmeter-${JMETER_VERSION}.tgz \
 && tar xzf apache-jmeter-${JMETER_VERSION}.tgz \
 && rm apache-jmeter-${JMETER_VERSION}.tgz
RUN ln -s /opt/apache-jmeter-${JMETER_VERSION}/bin/jmeter /usr/local/bin
RUN mkdir file
COPY ./start.sh /usr/local/bin
WORKDIR /file
ENTRYPOINT ["/usr/local/bin/start.sh"]
#CMD [ "/bin/sh" ]

