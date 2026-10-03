# Book Management CRUD

## Deployment URL

Vercel URL:

## Key Learning

- JavaScript DOM을 사용하여 HTML 요소를 만들고 화면에 출력하는 방법을 배웠다.
- JavaScript Array를 이용하여 데이터를 저장하고 관리하는 방법을 배웠다.
- addEventListener를 사용하여 버튼과 form에 이벤트를 연결하는 방법을 배웠다.
- CRUD 기능을 직접 구현하면서 Create, Read, Update, Delete의 과정을 이해했다.
- 입력값을 확인하고 잘못된 입력을 처리하는 방법을 배웠다.

## CRUD Details

### Create
사용자가 제목, 저자, 카테고리, 가격, 출판연도를 입력하면 새로운 책이 배열에 추가된다.

### Read
페이지가 실행되면 JavaScript Array에 저장된 책 목록이 화면에 출력된다.

### Update
Update 버튼을 누르면 선택한 책의 정보가 입력창에 나타난다.
내용을 수정한 후 저장하면 기존 책의 정보가 수정된다.

### Delete
Delete 버튼을 누르면 확인창이 나타난다.
확인을 누르면 해당 책이 배열에서 삭제되고 목록이 다시 출력된다.

## JavaScript Functions

### renderBooks()

JavaScript Array에 저장된 책 데이터를 화면에 출력한다.

### addEventListener()

버튼 클릭이나 form 제출과 같은 사용자의 동작을 처리한다.

### filter()

삭제할 책을 제외한 데이터를 다시 배열에 저장하는 데 사용했다.

### forEach()

배열에 있는 책 데이터를 하나씩 확인하고 화면에 출력하거나 수정할 때 사용했다.

### push()

새로운 책을 배열에 추가할 때 사용했다.

## AI / Search Usage

이번 과제에서는 JavaScript CRUD 기능을 구현하는 과정에서 AI를 참고하였다.

AI에게 JavaScript DOM, Event, Array를 이용한 CRUD 기능의 구현 방법을 질문하고, 코드에서 오류가 발생했을 때 원인과 해결 방법을 확인하였다.

특히 다음과 같은 부분에서 AI를 활용하였다.

- JavaScript Array에 초기 데이터를 저장하는 방법
- createElement와 appendChild를 이용하여 책 목록을 화면에 출력하는 방법
- addEventListener를 이용하여 Add, Update, Delete 버튼에 이벤트를 연결하는 방법
- push()를 이용하여 새로운 책을 배열에 추가하는 방법
- filter()를 이용하여 선택한 책을 삭제하는 방법
- Update 버튼을 눌렀을 때 기존 데이터를 입력창에 가져오는 방법
- 입력값이 비어 있는지 확인하는 validation 방법
- 삭제 후 새로운 책을 추가할 때 ID가 중복되는 문제의 원인과 해결 방법

AI가 제시한 코드를 그대로 사용하지 않고, 수업에서 실습한 createElement, appendChild, addEventListener 등의 방식과 비교하면서 이해한 후 코드에 적용하였다. 또한 각 기능을 직접 실행하고 오류가 발생하면 수정하면서 완성하였다.

AI를 통해 모르는 문법과 구현 방법을 참고했지만, 최종 코드는 직접 작성하고 테스트하였다.

## Problem & Solution

### Problem 1. JavaScript로 만든 책 목록이 처음에 화면에 나타나지 않았다.

JavaScript가 실행되는 위치와 HTML 요소가 만들어지는 순서를 확인했다.
script를 body의 bookList 아래에 배치하고 renderBooks()를 실행하여 해결했다.

### Problem 2. Update와 Add를 구분하는 것이 어려웠다.

updateId 변수를 사용하여 현재 수정 중인 책의 ID를 저장했다.
updateId가 0이면 새로운 책을 추가하고, 값이 있으면 기존 책을 수정하도록 구현했다.

### Problem 3. 책을 삭제한 후 새 책을 추가하면 ID가 중복될 수 있었다.

책의 개수를 이용하여 ID를 만드는 방식에서 별도의 newId를 사용하도록 수정했다.
새로운 책을 추가할 때마다 newId를 증가시켜 기존 ID와 겹치지 않도록 했다.

## Reflection

이번 과제를 통해 JavaScript의 DOM과 Event를 직접 사용해 볼 수 있었다.

처음에는 배열에 저장된 데이터를 화면에 출력하는 것도 어려웠지만, createElement와 appendChild를 사용하면서 HTML 요소를 JavaScript로 만드는 방법을 이해할 수 있었다.

또한 Create, Read, Update, Delete 기능을 직접 구현하면서 배열이 간단한 데이터 저장소처럼 사용될 수 있다는 것을 알게 되었다.

특히 Update 기능을 구현하면서 버튼을 클릭했을 때 기존 데이터를 입력창에 가져오고 다시 배열의 데이터를 수정하는 과정이 어려웠지만, 직접 테스트하면서 CRUD의 동작 과정을 이해할 수 있었다.