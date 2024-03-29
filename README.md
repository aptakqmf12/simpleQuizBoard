# command

- `npm run dev` : dev모드 실행(use turbopack)
- `npm run test:watch` : jest 실행
- `npm run storybook` : storybook 실행 (6006 port)

# Directory (src내부)

- `app` : next의 app router
- `api` : rest api
- `store` : zustand store
- `stories` : 공통 컴포넌트를 테스트할 storybook
- `util` : 기타 유틸로직들

# Test

## 단위 테스트 (@testing-library)

- `app/main.test.tsx`

  - [x] 렌더링시 버튼의 존재여부 확인
  - [ ] "퀴즈풀기" 버튼 클릭시 quiz 페이지로 이동 하는지 확인

- `app/quiz/quiz.test.tsx`

  - [ ] api 요청 실패시 alert 확인

- `app/quiz/_component/quizBoard.test.tsx`

  - [x] 렌더링시 title, answer의 개수가 알맞게 나오고 클릭전에 다음버튼이 나오지않는지 확인
  - [ ] 지문을 하나 클릭시에 해당 지문만 하이라이트되고, 다음버튼이 나오는지 확인
  - [ ] 다음버튼 클릭시 다음 지문이 나오는지 확인

- `app/quiz/_component/resultBoard.test.tsx`
  - [x] 렌더링시 최종 스코어, 전체 문제 리스트, 스코어에 대한 차트가 잘 나오는 지확인

## 컴포넌트 테스트 (Stroybook)

- Button : 사이즈, 배경색, 글자색, 비활성화 테스트
- Toast : 성공, 실패시 테스트
- DoughnutChart : 사이즈, 정답 및 오답 score에 따른 차트변화, legend사용유무 테스트
