# Overview
https://github.com/SungJinYoo/naver-gw-kit 을 fork받아 고쳤습니다.
- rlogin에서 ssh로 교체
- gateway에서 사용하던 스크립트를 Mac 터미널에서 사용 할 수 있도록 교체
- 그밖에 자잘한 버그 수정

# Env
Mac OS Mojave

# Usage
#### script에 실행 권한 부여
```
chmod 755 gwk.sh
```

#### remote user 추가
- ssh 접속에 사용할 remote user의 이름을 추가해줍니다. (21번 줄)
```
USER_LIST_FOR_LOGIN=(remote_user1 remote_user2)
```

#### .known_host 작성
- 자주 접속하는 서버의 호스트명을 작성합니다.
```
서버호스트명  설명
blahblah.github.com     example hostname
```

#### script 실행
```
./gwk.sh [커버로스 아이디] // 커버로스 인증과 동시에 쉘 실행
```

or
```
kinit
./gwk.sh
```
- 최초 커버로스 인증 이후엔 비밀번호를 입력하지 않고 엔터로 넘어가도 됩니다.
