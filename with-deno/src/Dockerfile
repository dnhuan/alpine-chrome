FROM ghcr.io/dnhuan/alpine-chrome:with-deno

RUN git clone https://github.com/puppeteer/puppeteer/blob/master/src/ puppeteer

ENTRYPOINT ["deno"]
CMD ["run", "https://deno.land/std/examples/welcome.ts"]
