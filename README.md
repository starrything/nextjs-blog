This is a starter template for [Learn Next.js](https://nextjs.org/learn).

# 1. Setup  
```
npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/basics-final"
```  

- public/images/profile.jpg with your photo (Recommended: 400px width/height).
- const name = '[Your Name]' in components/layout.js with your name.
- <p>[Your Self Introduction]</p> in pages/index.js with your self introduction.

# 2. Create tsconfig.json
프로젝트 루트에 tsconfig.json 파일을 생성합니다.  

터미널에서 아래 명령어를 실행합니다.
```
# If you’re using npm
npm install --save-dev typescript @types/react @types/node

# If you’re using Yarn
yarn add --dev typescript @types/react @types/node
```

아래 2개 파일을 확인해 보세요.  
- tsconfig.json : "moduleResolution": "node", "resolveJsonModule": true, 속성을 확인합니다.  
- next-env.d.ts  

# 3. Next.js 특정 유형들
## Static Generation & Server-side Rendering
```
import { GetStaticProps, GetStaticPaths, GetServerSideProps } from 'next';

export const getStaticProps: GetStaticProps = async (context) => {
  // ...
};

export const getStaticPaths: GetStaticPaths = async () => {
  // ...
};

export const getServerSideProps: GetServerSideProps = async (context) => {
  // ...
};
```

## API Routes
```
import { NextApiRequest, NextApiResponse } from 'next';

export default (req: NextApiRequest, res: NextApiResponse) => {
  // ...
};
```

## Custom 'App'
'page/_app.tsx' - 빌트인 타입(AppProps)

```
import { AppProps } from 'next/app';

function App({ Component, pageProps }: AppProps) {
  return <Component {...pageProps} />;
}

export default App;
```