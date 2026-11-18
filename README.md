# Todo Tutorial

[Claude Code Playbook](https://docs.claude-hunt.com) 강의에서 작은 할 일 앱을 직접 만들어 보며 Claude Code 쓰는 법을 배우는 연습용 저장소입니다.

## 관련 링크

- 강의 본문: https://docs.claude-hunt.com
- 수강생 결과물 공유: https://claude-hunt.com

## 기술 스택

- Next.js 16 (App Router, Turbopack)
- React 19
- Tailwind CSS v4
- shadcn/ui (radix-maia 스타일, taupe 베이스)
- TypeScript / ESLint / Prettier
- 패키지 매니저: bun 1.3.6

## 시작하기

### 준비물

- [Git](https://git-scm.com)
- [Bun](https://bun.sh) 1.3.6 이상 (`bun -v`로 확인). 이 저장소는 `bun.lock`을 쓰므로 npm이나 yarn 대신 bun으로 설치합니다.
- [Node.js](https://nodejs.org) 20.9 이상 (`node -v`로 확인). Next.js 16이 요구하는 버전입니다.

### 설치와 실행

```bash
git clone <저장소 주소>
cd todo-tutorial
bun install
bun dev
```

1. `git clone`과 `cd`로 저장소를 받아 폴더로 들어갑니다.
2. `bun install`로 의존성을 설치합니다.
3. `bun dev`로 개발 서버를 켭니다. 터미널에 `Ready`가 보이면 브라우저에서 [http://localhost:3000](http://localhost:3000) 을 엽니다. 3000번 포트가 이미 쓰이면 Next.js가 다른 포트를 골라 터미널에 알려 줍니다.
4. 서버를 끄려면 터미널에서 `Ctrl+C`를 누릅니다.

### 자주 쓰는 스크립트

```bash
bun run build      # 프로덕션 빌드
bun run start      # 빌드 결과 실행 (먼저 build가 필요합니다)
bun run lint       # ESLint
bun run typecheck  # tsc --noEmit
bun run test       # Vitest 테스트 1회 실행
bun run format     # Prettier 포맷팅
```

## 레슨별 시작 브랜치

레슨마다 시작 시점의 코드를 `lesson/<레슨 이름>` 브랜치로 제공합니다. 레슨 본문이 안내하는 브랜치로 바꾼 뒤 따라가세요.

```shell
git checkout lesson/claude-md
```

## 컴포넌트 추가

shadcn/ui 컴포넌트는 다음과 같이 추가합니다.

```bash
bunx --bun shadcn@latest add button
```

`components/ui` 디렉토리에 컴포넌트가 추가됩니다.

## 컴포넌트 사용

```tsx
import { Button } from "@/components/ui/button";
```
