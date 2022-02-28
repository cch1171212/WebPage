1. 세팅
	pip install django-embed-video
	pip install pillow
	설치

	1-1 makemigrations / migrate 진행 후 어드민 사이트 접속
	1-2 어드민 계정 : ID >> admin / Password >> admin1234 으로 로그인 
		어드민계정 없을 경우 createsuperuser 로 어드민 계정 만들기

	1-3 어드민 사이트 >> Posts 접속 후 데이터 존재여부 확인
		
		데이터 없을 경우 cmd 창에서 프로젝트 경로까지 접속 후 아래 코드 입력 (복사 붙여넣기 가능)
		↓데이터 100개짜리 입력하기
		python -Xutf8 manage.py loaddata data_100.json

		↓데이터 816개짜리 입력하기
		python -Xutf8 manage.py loaddata data_816.json
		
		코드 입력 후 Installed 100 object(s) from 1 fixture(s) 혹은
		Installed 816 object(s) from 1 fixture(s) 문장 확인되면 데이터 입력 완료.
		
		※주의사항
		100개짜리 데이터 입력 후 816개짜리 데이터 입력 시 UNIQUE 에러 발생됩니다.
		데이터가 100개짜리로 입력되어있을 경우 어드민 사이트에서 모든 데이터 삭제 후 816개짜리 데이터 입력 진행 시 정상 진행가능.

	1-4 localhost:8000/jypprj/mainpage 접속 

2.계정
	2-1 어드민 계정 : ID >> admin	/ Password >> admin1234
	2-2 홈페이지 테스트계정 X >> 회원가입 진행하시면됩니다.

3.페이지
	아래의 페이지는 URL접속 경로이나 사이드 메뉴 혹은 검색창 검색 시 이용 가능합니다.

	3-1 메인페이지		localhost:8000/jypprj/mainpage
	3-2 회원가입 페이지  	localhost:8000/jypprj/registerpage
	3-3 로그인 페이지		localhost:8000/jypprj/loginpage
	3-4 회원정보 페이지	localhost:8000/jypprj/memberpage
	3-5 회원정보수정 페이지 	localhost:8000/jypprj/modify
	3-6 JYP차트 페이지	http://localhost:8000/jypprj/chartpage
	3-7 전체음악 페이지	http://localhost:8000/jypprj/allmusic
	3-8 검색 페이지		http://localhost:8000/jypprj/search?sword=검색어
	3-9 음악정보 페이지	http://localhost:8000/jypprj/musicpage?num=게시글번호

4. 세부사항
	4-1 회원가입 방어코드 >> 회원가입 시 ID 혹은 닉네임 중복을 위해 각종 방어코드 작성 
				ID 및 닉네임 중복확인 안할경우 회원가입 불가
	4-2 로그인 시 이전페이지로 이동 >> 검색 결과 페이지 혹은 음악정보 페이지에서 로그인 시 원래있던 페이지로 이동합니다.
	4-3 장르별 분류 >> 메인페이지의 최신음악 / 장르별 인기 항목은 분류해두었으며 
		데이터 100개만 추가 시 국외장르의 최신음악 없음.
	4-4 메인페이지 및 JYP 차트 >> 게시글의 조회수 순으로 1~10위 혹은 1~100위까지 표시
	4-5 음악정보 페이지로 이동 >> 앨범 이미지, 노래 제목를 클릭할 경우 해당 노래페이지로 이동합니다.
	4-6 댓글 기능 >> 각종 음악정보 페이지 하단에서 댓글 입력이 가능하며,
			자신이 입력한 댓글이 있을경우 삭제또한 가능합니다.
	4-7 회원정보페이지 >> 자신이 입력한 댓글이 있을경우 회원정보 페이지에서 댓글 작성 노래, 댓글 내용을 확인할 수 있습니다.

※ 주의
음악 정보 페이지 하단에는 유튜브 동영상 링크를 걸어두었는데 
가끔씩 동영상 이용이 불가하다고 나올 경우가 있습니다.


	