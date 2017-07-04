FROM microsoft/nanoserver
LABEL maintainer "Andy Clarke"
ADD https://s3.amazonaws.com/mountebank/v1.11/mountebank-v1.11.0-win-x64.zip /
RUN powershell -command Expand-Archive -Path mountebank-v1.11.0-win-x64.zip -DestinationPath /
WORKDIR mountebank-v1.11.0-win-x64

FROM magicweasel/mountebank:latest
COPY --from=0 mountebank-v1.11.0-win-x64 /
