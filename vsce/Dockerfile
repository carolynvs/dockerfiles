FROM node:stretch

RUN npm install -g vsce

VOLUME /app
WORKDIR /app
RUN useradd --create-home --shell /bin/bash yousr &&\
 usermod -aG sudo yousr &&\
 chown -R yousr:yousr /app
USER yousr

ENTRYPOINT ["vsce"]