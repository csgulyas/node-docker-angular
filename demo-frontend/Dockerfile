FROM node:12.18.4-alpine AS dev

EXPOSE 4242
EXPOSE 49153

USER node

RUN mkdir -p /home/node/.npm-global
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

RUN npm install -g @angular/cli
WORKDIR /app

CMD ["ng", "serve", "--port", "4242", "--host", "0.0.0.0", "--disable-host-check", "--poll", "1000"]