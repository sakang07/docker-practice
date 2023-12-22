# node 14 환경으로 시작
FROM node:14

# working directory는 /app
WORKDIR /app

# package.json을 복사한다
COPY package.json .

# npm install 명령어 실행
RUN npm install

COPY . .

# 통신을 위해 3000 포트를 컨테이너 외부로 연다(샘플 nodejs 앱은 3000포트에서 들어오는 요청을 수신대기하는 웹 서버를 생성하고 있다)
EXPOSE 3000

# node 명령으로 app.mjs 명령어 실행
CMD [ "node", "app.mjs" ]