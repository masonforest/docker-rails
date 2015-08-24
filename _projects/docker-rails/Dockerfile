FROM phusion/passenger-ruby22:0.9.15
ENV HOME /root
CMD ["/sbin/my_init"]

ENV PHANTOM_JS_VERSION 1.9.7-linux-x86_64

RUN apt-get update
RUN apt-get install -y curl bzip2 libfreetype6 libfontconfig

RUN curl -sSL https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-$PHANTOM_JS_VERSION.tar.bz2 | tar xjC /
RUN ln -s /phantomjs-$PHANTOM_JS_VERSION/bin/phantomjs /usr/local/bin

# Clean up APT when done.
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
