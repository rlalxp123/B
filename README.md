# ⚡ 피카츄 집찾아가기

길을 잃은 피카츄를 미로 끝의 집까지 데려다 주는 웹게임이에요. 빌드 과정 없이 `public/index.html` 하나로 동작하고, Cloudflare에 바로 배포할 수 있어요.

## 게임 방법
- 이동: 방향키 / WASD / 화면 드래그(스와이프) / 화면 아래 방향 버튼(누르고 있으면 계속 이동)
- 번개 ⚡를 모으면 별을 더 받아요 (전부 모으면 ★★★)
- 💡 힌트: 집까지 가는 길을 2.5초 보여줘요 (레벨마다 3번)
- 레벨이 오를수록 미로가 커져요

## Cloudflare에 배포하기

### 방법 1: 대시보드에서 GitHub 연결 (가장 쉬움, 폰으로도 가능)
1. https://dash.cloudflare.com → **Workers & Pages** → **Create** → **Import a repository**
2. 이 GitHub 레포를 선택
3. 빌드 명령은 비워두고, 배포 명령은 `npx wrangler deploy` (기본값) 그대로 두기
4. 배포가 끝나면 `https://pikachu-home.<계정>.workers.dev` 주소로 플레이

이후 이 브랜치에 푸시할 때마다 자동으로 다시 배포돼요.

### 방법 2: 내 컴퓨터에서 명령어로
```bash
npm install
npx wrangler login
npm run deploy
```

로컬 테스트: `npm run dev` → http://localhost:8787
