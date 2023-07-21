FROM alpine:3.10
LABEL maintainer="vikum1407@sdet"

ENV SSL_DISABLED true
ENV ONE_SHOT true

RUN apk update && \
    apk upgrade && \
    apk add --update openjdk8-jre wget tar bash && \
    && mkdir /scripts

ENV RESILIENCE_HOME /scripts

# Add Resilience to the Path
ENV PATH $RESILIENCE_HOME/bin:$PATH
