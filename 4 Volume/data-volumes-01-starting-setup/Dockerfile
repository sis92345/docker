FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

# Dockerfile_old_command 내부에서만 사용 가능한 ARG, ARG [ARG NAME]=[VALUE]
ARG DEFAULT_PORT=80
# ENVironment PORT ENV 설정, 디폴트 값은 80
ENV PORT $DEFAULT_PORT

EXPOSE $PORT

CMD [ "node" , "server.js" ]