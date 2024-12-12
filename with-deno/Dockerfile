FROM ghcr.io/dnhuan/alpine-chrome

USER root
RUN apk add --no-cache tini deno

USER chrome
ENTRYPOINT ["tini", "--"]
