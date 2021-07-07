FROM node:latest

USER node

WORKDIR /workspaces/react-tutorial

# chownなしだとroot権限でコピーされるため、node権限ではnpm installができない
COPY --chown=node:node package.json package-lock.json ./

RUN npm install && npm cache clean --force
