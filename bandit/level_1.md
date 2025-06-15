# Goal

bandit0 서버의 readme 파일에서 비밀번호 획득한 뒤  bandit1 서버로 접근
https://overthewire.org/wargames/bandit/bandit1.html

## Answer

- bandit0 서버에서 bandit1로 가는 비밀번호 확인

```shell
sshpass -p 'bandit0' ssh -p 2220 bandit0@bandit.labs.overthewire.org
cat readme # 비밀번호 확인
exit
```

- 연결 종료 후 bandit1 서버로 접근

```shell
sshpass -p 'new_password' ssh -p 2220 bandit1@bandit.labs.overthewire.org
```
