FROM node:alpine

# install angular cli dependencies
RUN apk update && apk upgrade && \
    apk add --no-cache git

# install angular-cli as node user - Wait because it take a while
RUN chown -R node:node /usr/local/lib/node_modules \
    && chown -R node:node /usr/local/bin

USER node
RUN yarn global add @angular/cli

# set yarn as default package manager for all users
RUN ng set --global packageManager=yarn

CMD ["ng"]
