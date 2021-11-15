https://user-images.githubusercontent.com/79011228/132659548-c4d22a0a-6fac-404f-b13d-5cb082c8d618.mov


## 기본 요구사항



## 구현 설명
+ 해당 리스트를 호버하면 삭제와 추가 버튼이 생깁니다.
+ 해당 리스트를 선택하면 제목과 내요을 편집 할 수 있습니다.
+ 토글버튼을 누르면 하위 파일들이 나옵니다.
+ 삭제버튼을 누르면 하위 파일까지 삭제하냐고 한번 확인을 합니다 (yes => 하위 파일까지 삭제/ no => 현재 문서만 삭제)
+ 글 단위를 Document라고 합니다. Document는 Document 여러개를 포함할 수 있습니다.
+ 화면 좌측에 Root Documents를 불러오는 API를 통해 루트 Documents를 렌더링합니다.
+ Root Document를 클릭하면 오른쪽 편집기 영역에 해당 Document의 Content를 렌더링합니다.
+ 해당 Root Document에 하위 Document가 있는 경우, 해당 Document 아래에 트리 형태로 렌더링 합니다.
+ Document Tree에서 각 Document 우측에는 + 버튼이 있습니다. 해당 버튼을 클릭하면, 클릭한 Document의 하위 Document로 새 
        Document를 생성하고 편집화면으로 넘깁니다.
+ 편집기에는 기본적으로 저장 버튼이 없습니다. Document Save API를 이용해 지속적으로 서버에 저장되도록 합니다.
+ History API를 이용해 SPA 형태로 만듭니다.
+ /documents/{documentId} 로 접속시, 해당 Document 의 content를 불러와 편집기에 로딩합니다.

## 개선점 
+ 하위파일을 삭제할 때, 바로 아랫단위의 파일들만 삭제됨 -> 전체삭제 가능하게 개선해야 합니다.
+ 하위 파일이 없어도 하위파일까지 삭제하나고 확인함 -> 하위 파일의 존재 여부에 따라 질문이 바뀌어야함
+ color팔렛트를 만들어 테마 색상을 바꾸고 싶었지만 구현하지 못했다.
