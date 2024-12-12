ARG NODE_VERSION=18.20.5
FROM node:${NODE_VERSION}-alpine AS node

FROM ghcr.io/dnhuan/alpine-chrome

COPY --from=node /usr/lib /usr/lib
COPY --from=node /usr/local/lib /usr/local/lib
COPY --from=node /usr/local/include /usr/local/include
COPY --from=node /usr/local/bin /usr/local/bin

RUN node -v

USER root
RUN npm install -g yarn --force
RUN yarn -v

USER chrome
ENTRYPOINT ["tini", "--"]
