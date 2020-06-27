FROM clojure:boot-alpine

LABEL "com.github.actions.name"="zprint"
LABEL "com.github.actions.description"="Provides linting and fixes using zprint"
LABEL "com.github.actions.icon"="user-check"
LABEL "com.github.actions.color"="purple"

LABEL "repository"="http://github.com/bltavares/actions"
LABEL "homepage"="http://github.com/bltavares/actions"
LABEL "maintainer"="Bruno Tavares <connect+githubactions@bltavares.com>"

RUN echo '{:search-config? true}' >~/.zprint.edn \
  && boot -d boot-fmt -d zprint fmt --help >/dev/null
RUN apk --no-cache add curl jq bash git

COPY lib.sh /lib.sh
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
