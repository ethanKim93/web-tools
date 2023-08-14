# web-tools (web-tools)

online tools

## Install the dependencies
```bash
yarn
# or
npm install
```

### Start the app in development mode (hot-code reloading, error reporting, etc.)
```bash
quasar dev
```


### Lint the files
```bash
yarn lint
# or
npm run lint
```



### Build the app for production
```bash
quasar build
```

### Customize the configuration
See [Configuring quasar.config.js](https://v2.quasar.dev/quasar-cli-vite/quasar-config-js).


### eslint(standard 설정)
- settings.json에 아래 설정 추가 [참고 자료](https://stackoverflow.com/questions/68191278/vue-2-eslint-standard-prettier)
  ```
  {
    "editor.codeActionsOnSave": {
      "source.organizeImports": false,
      "source.fixAll": true,
      "source.fixAll.eslint": true,
      "source.fixAll.stylelint": true
    }
  }
  ```

### 폴더 구조
- Atomic Design Base의 구조를 따른다. 
  
  |단계|내용|UI 예시|
  |------|---|---|
  |Atoms	|이 이상 나눌 수 없는 단위	|버튼, 텍스트 입력란, 라벨|
  |Molecules	|Atoms를 여러개 합친 것	|입력폼(라벨 + 입력란)|
  |Organisms	|1개의 명확한 기능을 가진 것	|헤더|
  |Templates	|페이지의 틀을 구성하는 것	|와이어 프레임|
  |Pages	|페이지에 컨텐츠가 있는 것	|디자인 완성 견본|
  
- `Atoms`, `Molecules`, `Templates` 는 유저 인터페이스나, 부모 컴포넌트로 받은 데이터를 어덯게 표현할지에 전념한다.
- `Organisms`와 `Pages`는 컨텐츠에 관심이 높다. 즉, API나 store 등 데이터의 획득, 변경의 책임을 가진다.
- `Container`이라는 단계를 추가하여 Depth가 무의미하게 깊어질 경우 `더러운 컴포넌트`를 만들수 있다.
- 참고링크
  - [Atomic Design 베이스의 Vue 컴포넌트 설계](https://engineer-mole.tistory.com/331)
  - [Effective Atomic Design](https://kciter.so/posts/effective-atomic-design)
  - [Atomic Design 설계와 Container Component](https://univdev.page/posts/atomic-design-with-container-component/)
  - [기타 - Vue 폴더 구조](https://uminoh.tistory.com/50#Case%20Study%20%3A%20Components%20in%20Large%20Scale%20Application-1)


### 스토리북 
- 설치 
  - yarn 설치 
    ```
      npm install -g yarn
    ```
  - vite 추가 
    ```
      yarn add vite
    ```
  - story book 설치
    ```
    npx storybook@latest init
    ```
  - story book 실행 
    ```
      yarn storybook
    ```
- 참고
  - [Quasar,vite,pinia 환경 Storybook 설치](https://javascript.plainenglish.io/setup-storybook-for-the-quasar-project-vite-pinia-vue-i18n-69b41745af60)
  - [Vue3 프로젝트에 Storybook 7 설치, 적용하기](https://velog.io/@kdeun1/Vue3-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%97%90-Storybook-%EC%A0%81%EC%9A%A9%ED%95%98%EA%B8%B0)