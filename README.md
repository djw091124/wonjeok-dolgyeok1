# 원격돌격

브라우저에서 실행하는 원 전투 게임입니다. Node.js + WebSocket 서버를 사용하며 Render Web Service 배포를 전제로 합니다.

## 실행
1. Node.js 18 이상 설치
2. `npm install`
3. `npm start`
4. 브라우저에서 `http://localhost:3000` 열기

## Render 배포
- Runtime: Node
- Build Command: `npm install`
- Start Command: `npm start`
- Web Service로 배포해야 합니다.
- 온라인 매칭은 같은 배포 주소에 접속한 두 플레이어가 매칭을 시작해야 합니다.

## 현재 기능
- 메뉴: 유저 매칭, AI 매칭, 원 도감, 원 트로피
- 스파이더맨 기본 지급, 망치보이는 트로피 50개 달성 시 해금
- 승리 +8 트로피, 패배 -4 트로피(최저 0)
- WASD 이동, 마우스 조준 및 공격, E를 누른 채 클릭하면 궁극기 사용
- 회원가입/로그인 UI 및 브라우저 로컬 저장

## 저장 관련 주의
현재 로그인/계정/전적 데이터는 브라우저의 `localStorage`에 저장됩니다. 따라서 같은 브라우저/기기에서는 유지되지만, 다른 기기와 자동 동기화되지 않으며 브라우저 데이터를 지우면 사라질 수 있습니다. Render 서버의 `accounts.json`이나 데이터베이스에 저장되는 서버 계정 시스템은 이 패키지에 아직 구현되어 있지 않습니다. 영구적인 다기기 저장을 위해서는 서버 인증 API와 영구 데이터베이스(또는 Render Persistent Disk)를 추가해야 합니다.
