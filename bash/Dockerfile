FROM alpine

LABEL "com.github.actions.name"="bash"
LABEL "com.github.actions.description"="Provides shell utilities such as curl and make"
LABEL "com.github.actions.icon"="settings"
LABEL "com.github.actions.color"="yellow"

LABEL "repository"="http://github.com/bltavares/actions"
LABEL "homepage"="http://github.com/bltavares/actions"
LABEL "maintainer"="Bruno Tavares <connect+githubactions@bltavares.com>"

RUN apk --no-cache add curl wget jq bash git make binutils file zip

COPY lib.sh /lib.sh
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
