## git commit author 설정

최초에 컴퓨터에서 git을 활용하려고 하면, 아래의 설정을 하지 않으면 commit 이 안된다.

```bash
$ git config --global user.name __username__
$ git config --global user.email __username__
```

* 설정을 확인할 때는 아래의 명령어를 활용한다.

```bash
$ git config --global -l
user.name=song
user.email=shi9512@naver.com
```

* 설정된 이메일이 Github에 등로된 이메일이랑 같도록 하는것을 추천(잔디밭)

