# git 사용법
- git init - 초기화, 처음에만 하면 됨(저장소 안에 저장소를 넣으면 안됨 주의)
- git add [파일 이름]
- git commit -m "이름"
- git status - 현재상태 확인 빨강 - 워킹 디렉토리, 초록 - 스테이징
- git log - commit 목록보기(한줄은 --oneline 추가)

# git 저장소 추가
- git remote add origin [주소](물결있으면 지우기)
- git push origin(저장소 이름) master(가지)
- git pull origin master
- git clone [https: 주소 ]
- git remote -v(저장소 목록)

# git 사용자 바꾸기
- git config --global user.email "name@naver.com"
- git config --unset user.email
- git config —global -l (list) - git global 설정 정보 보기


# gitignore
- gitignore(특정 파일이나 디렉토리 추적x - 텍스트 파일임)(파일명앞에 . 확장자 없음) - gitigonore.io(싸이트)
