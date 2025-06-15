## Goal

'-' 이름의 파일에 있는 비밀번호 찾아서 bandit2 서버로 접근
https://overthewire.org/wargames/bandit/bandit2.html

## Answer

- bandit1 서버에서 bandit2로 가는 비밀번호 확인

```shell
sshpass -p 'new_password' ssh -p 2220 bandit1@bandit.labs.overthewire.org
cat ~/- # 비밀번호 확인
exit
```

- 연결 종료 후 bandit2 서버로 접근

```shell
sshpass -p '263JGJPfgU6LtdEvgfWU1XP5yac29mFx' ssh -p 2220 bandit2@bandit.labs.overthewire.org
```

## What I Learned

- 리눅스에서 대시는 옵션으로 인식됨
- 파일명으로 쓰게 되면 `./`나 `~/`를 앞에 붙여서 뒤에 오는 글자가 파일이라는 걸 알려줘야함
- `--`를 붙이면 뒤에 오는 이름은 무조건 파일명으로 인식함
