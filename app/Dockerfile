# 1. 명시적인 Node.js LTS 버전과 가벼운 alpine 이미지 사용 (버전 고정)
FROM node:22-alpine 

# 2. 컨테이너 내부 작업 디렉토리 설정
WORKDIR /app

# 7. 컨테이너가 사용할 포트 명시
EXPOSE 3000

# 8. 프로덕션 서버 실행 명령어
CMD ["npm", "run", "start"]