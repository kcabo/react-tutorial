FROM node:latest

USER node

# chownなしだとroot権限でコピーされるため、node権限ではnpm installができない
COPY --chown=node:node package.json package-lock.json ./

RUN npm install && npm cache clean --force
