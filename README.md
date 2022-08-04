# myblog_javascript

## API 명세서

| 기능 | API URL | Method | 입력|
| ------ | ------ | ------ | ------ |
| 회원 가입 | /users/signup | POST | **body** <br>{nickname, <br>password, <br>confirm} | 
| 로그인 | /users/login | POST | **body** <br>{nickname, <br>password} |
|  |  |  | | 
| 게시글 작성 | /posts | POST | **body** <br>{title,  <br>content} | 
| 게시글 조회 | /posts | GET | | 
| 게시글 상세조회 | /posts/:postId | GET | | 
| 게시글 수정 | /posts/:postId | PUT | **body** <br>{title, <br>content} | 
| 게시글 삭제 | /posts/:postId | DELETE | | 
|  |  |  | | 
| 댓글 생성 | /posts/:postId/comments | POST | **body** <br>{content} | 
| 댓글 목록 조회 | /posts/:postId/comments | GET | | 
| 댓글 수정 | /posts/:postId/comments/:commentId | PUT | **body** <br>{content} | 
| 댓글 삭제 | /posts/:postId/comments/:commentId | DELETE | | 
|  |  |  | | 
| 게시글 좋아요 | /posts/:postId/like | PATCH |  | 
| 좋아요 게시글 조회 | /posts/like | GET | | 


테스트시 로그인의 경우, 발급된 JWT 토큰을 req.header의 Authorization 에 넣어주었습니다.
기본 포맷은 "Bearer ${jwt 토큰}" 입니다.
