# cloudmemoapi

데이터 구조

    content (메모 내용)
    created_at (생성 시간) 
    updated_at (수정 시간)
    deleted_at (제거 시간)
 

GET

* "/"  - 모든 메모 가져오기 (단, delete_at이 null이 아니면 출력하지 않는다)
* "/:id" - 단일 메모 가져오기 (만약 delete_at이 null이 아닌 경우 오류메시지 출력)
* "tmp" - 임시 저장된 데이터 가져오기 (작성하고 생성하지는 않았지만 임시로 저장해놓는 데이터로, 서버를 재시작하면 초기화됨)

POST

* "/" - 메모 생성하기

DELETE 

* "/" - 전체 메모 제거하기 (전체 메모의 `delete_at`에 현재 시간을 추가함)
* "/:id" - 단일 메모 제거하기 (실질적으로 제거되는 것이 아니라 `delete_at`에 시간을 추가함)


PUT

* "/:id" - 단일 메모 수정하기   

