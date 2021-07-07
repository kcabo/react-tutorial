FROM node:latest

USER node

WORKDIR /workspaces/react-tutorial

# chownなしだとroot権限でコピーされるため、node権限ではnpm installができない
COPY --chown=node:node package.json package-lock.json ./

RUN npm install && npm cache clean --force

# Volume Trick
VOLUME /workspaces/react-tutorial/node_modules

EXPOSE 3000

ENV TZ Asia/Tokyo