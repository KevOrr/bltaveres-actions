FROM mcr.microsoft.com/powershell:alpine-3.10

LABEL "com.github.actions.name"="pwshfmt"
LABEL "com.github.actions.description"="Provides Powershell formatter using PowerShell-Beautifier"
LABEL "com.github.actions.icon"="user-check"
LABEL "com.github.actions.color"="purple"

LABEL "repository"="http://github.com/bltavares/actions"
LABEL "homepage"="http://github.com/bltavares/actions"
LABEL "maintainer"="Bruno Tavares <connect+githubactions@bltavares.com>"

RUN pwsh -c 'Install-Module -Name PowerShell-Beautifier -Force'
RUN pwsh -c 'Import-Module PowerShell-Beautifier.psd1'

RUN apk --no-cache add curl jq bash git

COPY lib.sh /lib.sh
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
