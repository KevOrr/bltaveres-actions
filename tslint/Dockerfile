FROM node:alpine

LABEL "com.github.actions.name"="tslint"
LABEL "com.github.actions.description"="Provides linting for TypeScript files"
LABEL "com.github.actions.icon"="user-check"
LABEL "com.github.actions.color"="purple"

LABEL "repository"="http://github.com/bltavares/actions"
LABEL "homepage"="http://github.com/bltavares/actions"
LABEL "maintainer"="Bruno Tavares <connect+githubactions@bltavares.com>"

RUN npm install -g tslint typescript codelyzer

RUN apk --no-cache add curl jq bash git

COPY lib.sh /lib.sh
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
