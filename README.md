# AI 게임잼 2024 쇼케이스

AI 게임잼 2024에서 출품된 혁신적인 게임들을 소개하는 웹사이트입니다.

## 📋 프로젝트 개요

이 프로젝트는 AI 기술을 활용한 게임 개발 컨테스트의 출품작들을 효과적으로 소개하기 위한 반응형 웹 애플리케이션입니다.

### 주요 기능

- 🎮 **게임 카드 기반 레이아웃**: 각 게임을 카드 형태로 표시
- 📱 **반응형 디자인**: 모바일, 태블릿, 데스크톱 지원
- 🎥 **미디어 갤러리**: YouTube 영상, 이미지, WebP 파일 지원
- ⚡ **인터랙티브 모달**: 게임 상세 정보 팝업
- 🎨 **세련된 UI/UX**: 게임잼 분위기에 맞는 밝고 현대적인 디자인
- 🎯 **SVG 애니메이션**: 시각적 포인트를 위한 커스텀 SVG 요소들

## 🛠️ 기술 스택

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Animation**: Framer Motion
- **Deployment**: Vercel (예정)

## 🚀 설치 및 실행

### 1. 의존성 설치

```bash
npm install
```

### 2. 개발 서버 실행

```bash
npm run dev
```

브라우저에서 [http://localhost:3000](http://localhost:3000)을 열어 확인하세요.

### 3. 빌드

```bash
npm run build
```

### 4. 프로덕션 실행

```bash
npm start
```

## 📁 프로젝트 구조

```
ai-gamejam-showcase/
├── app/                    # Next.js App Router
│   ├── globals.css        # 글로벌 스타일
│   ├── layout.tsx         # 메인 레이아웃
│   └── page.tsx           # 홈페이지
├── components/            # React 컴포넌트
│   ├── header.tsx         # 헤더 컴포넌트
│   ├── game-card.tsx      # 게임 카드 컴포넌트
│   └── game-modal.tsx     # 게임 상세 모달
├── data/                  # 데이터 파일
│   └── games.ts           # 게임 데이터
├── types/                 # TypeScript 타입 정의
│   └── game.ts            # 게임 관련 타입
├── next.config.js         # Next.js 설정
├── tailwind.config.js     # Tailwind CSS 설정
└── tsconfig.json          # TypeScript 설정
```

## 🎮 게임 데이터 형식

```typescript
interface Game {
  id: string;
  name: string;
  genre: string;
  platform: string[];
  description: string;
  thumbnail: string;
  media: GameMedia[];
  features?: string[];
  developers: string[];
  tags: string[];
  createdAt: string;
}

interface GameMedia {
  type: 'youtube' | 'image' | 'webp';
  url: string;
  title?: string;
  thumbnail?: string;
}
```

## 🎨 디자인 특징

### 컬러 팔레트
- **Primary**: Purple & Blue Gradients
- **Secondary**: Warm accent colors
- **Background**: Light gradients with glass effects

### 애니메이션
- **Hover Effects**: 카드 확대 및 그림자 효과
- **Float Animation**: SVG 요소들의 부유 애니메이션
- **Glow Effects**: 버튼 및 아이콘 글로우 효과

### 반응형 브레이크포인트
- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

## 📝 게임 데이터 수정

새로운 게임을 추가하거나 기존 게임 정보를 수정하려면 `data/games.ts` 파일을 편집하세요:

```typescript
export const sampleGames: Game[] = [
  {
    id: 'your-game-id',
    name: '게임 이름',
    genre: '장르',
    platform: ['Web', 'Mobile', 'PC'],
    description: '게임 설명...',
    thumbnail: '/images/thumbnail.jpg',
    media: [
      {
        type: 'youtube',
        url: 'https://youtube.com/watch?v=...',
        title: '게임플레이 영상'
      }
    ],
    // ... 기타 필드들
  }
]
```

## 🚀 Vercel 배포

1. GitHub에 코드 푸시
2. Vercel에서 저장소 연결
3. 자동 빌드 및 배포

## 🎯 주요 컴포넌트

### Header
- 프로젝트 브랜딩
- 이벤트 정보 표시
- 반응형 네비게이션

### GameCard
- 게임 썸네일 및 기본 정보
- 호버 인터랙션
- 플랫폼 아이콘 표시

### GameModal
- 게임 상세 정보
- 미디어 갤러리 (이미지/영상)
- 스크롤 가능한 콘텐츠

## 🔧 커스터마이징

### 색상 변경
`tailwind.config.js`와 `app/globals.css`에서 색상 팔레트를 조정할 수 있습니다.

### 애니메이션 조정
`tailwind.config.js`의 `keyframes`와 `animation` 섹션에서 애니메이션을 수정할 수 있습니다.

### 레이아웃 변경
컴포넌트 파일들을 직접 편집하여 레이아웃을 원하는 대로 조정할 수 있습니다.

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 제공됩니다.

## 🤝 기여

버그 신고, 기능 제안, 풀 리퀘스트 모두 환영합니다!

---

**AI 게임잼 2024** - 인공지능과 게임 개발의 혁신적인 만남 🎮✨ 