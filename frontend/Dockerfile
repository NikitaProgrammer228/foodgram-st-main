# build env
FROM node:21.7.1-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --legacy-peer-deps --progress=false --fetch-retries=5 --fetch-retry-factor=2
COPY . ./
RUN npm run build
CMD cp -r build result_build
