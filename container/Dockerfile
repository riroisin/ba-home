# 1. 명시적인 Node.js LTS 버전과 가벼운 alpine 이미지 사용 (버전 고정)
FROM node:22-alpine 

# 2. 컨테이너 내부 작업 디렉토리 설정
WORKDIR /app

# 3. Next.js 프로젝트 자동 생성 (사람의 입력 없이 기본값으로 강제 설치)
# --yes : 설치 확인 건너뛰기
# --use-npm, --typescript 등 : 설정 프롬프트 건너뛰기
RUN npx create-next-app@latest . \
    --use-npm \
    --yes \
    --typescript \
    --tailwind \
    --eslint \
    --app \
    --src-dir=false \
    --import-alias="@/*"

# 6. Next.js 프로덕션 빌드 (최적화된 정적 파일 및 서버 코드 생성)
RUN npm run build

# 7. 컨테이너가 사용할 포트 명시
EXPOSE 3000

# 8. 프로덕션 서버 실행 명령어
CMD ["npm", "run", "start"]