<h4>1단계: 회원가입/로그인</h4>
  <p>User 엔티티, 리포지토리, 서비스, 컨트롤러 생성</p>
  <p>Spring Security + JWT 설정 (비밀번호 암호화 필수!)
  <p>POST /api/signup (회원가입), POST /api/login (로그인) API 구현
  <p>signup.html, login.html 만들고 fetch()로 API 연동
  <p>로그인 성공 시 JWT 토큰을 localStorage에 저장

<h4>2단계: 게시글 CRUD</h4>
  <p>Post 엔티티 및 관련 모듈 생성
  <p>POST /api/posts (글쓰기), GET /api/posts (모든 글 조회) API 구현
  <p>index.html에 글쓰기 폼 생성, fetch() 연동 (이때 헤더에 JWT 토큰 첨부)
  <p>index.html 로드 시 fetch()로 글 목록 불러와서 동적 렌더링 (위 JS 예시 참고)

<h4>3단계: 팔로우 & 타임라인</h4>
  <p>Follow 엔티티 및 관련 모듈 생성
  <p>POST /api/users/{userId}/follow (팔로우), DELETE ... (언팔로우) API 구현
  <p>(핵심) GET /api/posts/timeline API 수정: 기존 '모든 글'이 아닌, '내가 팔로우한 사람들의 글'만 가져오도록 로직 변경 (JPA 쿼리 필요)
  <p>프로필 페이지에서 팔로우/언팔로우 버튼 구현

<h4>4단계: 좋아요</h4>
  <p>Likes 엔티티 및 관련 모듈 생성
  <p>POST /api/posts/{postId}/like (좋아요), DELETE ... (좋아요 취소) API 구현
  <p>게시글 카드에 '좋아요' 버튼 추가, fetch() 연동 및 좋아요 수 동적 업데이트
