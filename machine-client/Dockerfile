FROM node:14.15-alpine

WORKDIR /app

ENV NODE_ENV="production"
COPY ./package.json ./package-lock.json ./
RUN npm install \
&& npm cache clean --force

COPY . .

USER 1000
ENTRYPOINT ["node"]
CMD ["--eval='process.exit(0);'"]
EXPOSE 8080
