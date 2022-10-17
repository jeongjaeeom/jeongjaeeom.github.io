---
title: "리눅스 서버 터미널 기본 설정"
description:
date: 2022-10-17
update: 2022-10-17
tags:
- linux
- terminal
- shell
- aws
---


# 리눅스 서버 터미널 기본 설정
리눅스 서버 설치 후 기본적인 터미널 설정을 진행해봅니다.  
`AWS EC2` 환경에서 `Amazon Linux 2`를 설치하여 진행하였습니다.

## 터미널 세션 타임아웃(Sessio Timeout) 설정
Sessio Timeout을 설정 하여 일정 시간 작업을 하지 않을 경우 터미널 연결을 해제 하도록 설정할 수 있습니다.

프로파일(.profile) 파일 생성 및 내용 입력
```shell
$ sudo vi ~/.profile
HISTTIMEFORMAT="%F %T -- "
export HISTTIMEFORMAT
export TMOUT=600 

$ source ~/.profile
```
* `HISTTIMEFORMAT` - history 명령 결과에 시간 값을 추가한다.
* `TMOUT=600` - 세션 타임아웃을 설정한다(초 단위).


## 쉘(Shell) Prompt 변경하기
Bastion 서버 등과 같이 서버를 구분해야하는 경우에 Shell Prompt를 설정하여 서버 관리자의 인적 장애를 예방할 수 있다.

```shell
$ sudo vi ~/.bashrc
USERNAME=BASTION
PS1='[\e[1;31m$USERNAME\e[0m][\e[1;32m\t\e[0m][\e[1;33m\u\e[0m@\e[1;36m\h\e[0m \w] \n\$ \[\033[00m\]'

$ source ~/.bashrc
```

## Logger를 사용하여 감사로그 남기기
서버에서 작업할 경우, 작업 이력 히스토리를 기록해 두어야 장애 발싱시 원인 분석을 할 수 있습니다.

```shell
$ sudo vi ~/.bashrc
tty=`tty | awk -F"/dev/" '{print $2}'`
IP=`w | grep "$tty" | awk '{print $3}'`
export PROMPT_COMMAND='logger -p local0.debug "[USER]$(whoami) [IP]$IP [PID]$$ [PWD]`pwd` [COMMAND] $(history 1 | sed "s/^[ ]*[0-9]\+[ ]*//" )"'

$ source  ~/.bashrc
```

```shell
$ sudo vi /etc/rsyslog.d/50-default.conf
local0.*  /var/log/command.log

$ sudo service rsyslog restart
$ tail -f /var/log/command.log
```
## 참고
* [인프라 공방](https://edu.nextstep.camp/c/VI4PhjPA/)
