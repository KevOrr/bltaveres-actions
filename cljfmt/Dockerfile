FROM clojure:tools-deps-alpine

LABEL "com.github.actions.name"="cljfmt"
LABEL "com.github.actions.description"="Provides linting and fixes using cljfmt"
LABEL "com.github.actions.icon"="user-check"
LABEL "com.github.actions.color"="purple"

LABEL "repository"="http://github.com/bltavares/actions"
LABEL "homepage"="http://github.com/bltavares/actions"
LABEL "maintainer"="Bruno Tavares <connect+githubactions@bltavares.com>"

RUN clojure -Sdeps '{:deps {lein-cljfmt {:mvn/version "LATEST"}}}' -e ':ok'

RUN apk --no-cache add curl jq bash git

COPY lib.sh /lib.sh
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
