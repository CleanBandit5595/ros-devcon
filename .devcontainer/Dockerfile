FROM ros-dev-base:latest

#https://update.code.visualstudio.com/commit:8fa188b2b301d36553cbc9ce1b0a146ccb93351f/server-linux-x64/stable
ARG COMMIT_ID="8fa188b2b301d36553cbc9ce1b0a146ccb93351f"

COPY vscode-server-linux-x64.tar.gz /tmp/
RUN mkdir -p ~/.vscode-server/bin/${COMMIT_ID}}
RUN tar zxvf /tmp/vscode-server-linux-x64.tar.gz -C ~/.vscode-server/bin/${COMMIT_ID}} --strip 1