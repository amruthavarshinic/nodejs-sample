FROM mcr.microsoft.com/windows/servercore:ltsc2019

RUN mkdir c:\\nodejs && \
    powershell -NoProfile -Command \
    $ErrorActionPreference = 'Stop'; \
    Invoke-WebRequest -Uri "https://nodejs.org/download/release/v12.22.3/node-v12.22.3-win-x64.zip" -OutFile "c:\\nodejs\\nodejs.zip" -UseBasicParsing ; \
    Expand-Archive -Path "c:\\nodejs\\nodejs.zip" -DestinationPath "c:\\nodejs" ; \
    Remove-Item -Path "c:\\nodejs\\nodejs.zip"

ENV PATH c:\\nodejs\\node-v12.22.3-win-x64\\;%PATH%