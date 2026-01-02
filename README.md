# Form CSS Styling Practice (폼 스타일 꾸미기)

수업 시간에 배운 CSS 선택자 + 폼(input) 스타일링을 적용해보는 실습입니다.  
`attribute selector`, `:focus`, `box-sizing` 등을 이용해 입력창 UI를 개선합니다.

---

## 1) 학습 목표

- `input[name="..."]` 같은 속성 선택자(attribute selector) 사용하기
- `:focus` 상태에서 포커스 스타일(밑줄 강조) 적용하기
- `width`, `padding`, `margin`, `box-sizing`으로 레이아웃 깨짐 방지하기
- `label for` + `input id`로 라벨 클릭 시 포커스 이동 연결하기

---

## 2) 핵심 포인트 정리

### (1) `:focus`가 반영되지 않는 대표 원인
- 라벨을 눌렀는데 `for=""`가 비어 있으면 input에 포커스가 안 들어감  
  → `label for="input2"` 와 `input id="input2"`를 연결해야 함

### (2) border-bottom을 안정적으로 주는 방법
- `:focus`에서 갑자기 border가 생기면 UI가 흔들릴 수 있음
- 기본 상태에서 `border-bottom`을 투명(transparent)으로 깔아두고,
  포커스에서 색만 바꾸면 안정적