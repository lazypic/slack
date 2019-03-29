# Slack
Lazypic은 채팅 솔루션으로 Slack을 사용합니다.

채널 : https://lazypic.slack.com

## Channel name
Slack channel names must be the same name as github repositories.

example
- https://github.com/lazypic/circle
- slack channel name : #circle

## Admin메뉴
Primary Owner가 최고 권한이며, 보통 맴버를 관리할 때 사용합니다.

https://lazypic.slack.com/admin

## 화상채팅
채널에서 아래처럼 타이핑합니다.

```
/hangout
```

## 보안이슈
보안이 중요한 프로젝트는 별도의 채널을 만들고 진행합니다.

## 이 리포지터리를 만든이유
Slack 기본 기능으로도 훌륭합니다.
몇몇 기능을 활용하면 프로젝트 진행시 조금 더 편리하게 커뮤니케이션을 할 수 있습니다.
그래서 Slack 셋팅방법을 다루는 리포지터를 생성했습니다.

## 방해금지모드 사용법
Slack을 사용하는 이유는 방해금지 시간, 기타툴의 연동등을 자유롭게 설정할 수 있기 때문입니다.
취침시간, 휴식시간등 자유롭게 설정하고 사용하세요.

![slack_setting01](https://user-images.githubusercontent.com/1149996/49338806-974a5f00-f66a-11e8-8df2-7acd35f808da.png)

![slack_setting02](https://user-images.githubusercontent.com/1149996/49338807-974a5f00-f66a-11e8-86b0-8806efc7a829.png)

![slack_setting03](https://user-images.githubusercontent.com/1149996/49338809-974a5f00-f66a-11e8-8867-14f1989df591.png)


## 채널설정
관리자 설정페이지 : https://lazypic.slack.com/customize

## New Respose 설정
https://lazypic.slack.com/customize/slackbot

## 개발툴과 Slack 연결하기
Slack의 Webhook 기능을 이용해서 다른 툴에서 채팅방으로 정보전달이 가능합니다.
여러분이 만든 프로그램과 Slack 채널이 연동되어야 한다면, Webhook 토큰이 필요합니다.
Webhook 토큰을 알고 싶다면 [admin@lazypic.org](mailto:admin@lazypic.org)로 메일주세요.
이미 슬렉채널에 가입되어있다면 `webhook` 이라고 채팅창에 타이핑하면 Webhook 토큰을 Slackbot이 알려줍니다.

- Webhook 설정페이지 : https://api.slack.com/apps/AEGKLE3T3/incoming-webhooks?success=1


#### Webhook + curl을 이용한 메시지 전송
curl을 이용해서 slack에 메시지를 보내는 예제이며, 각 channel마다 다른 token이 부여됩니다.
```
$ curl -X POST -H 'Content-type: application/json' --data '{"text":"Hello, Slack!"}' https://hooks.slack.com/service/{token}/{token}/{token}
```

지원하는 data의 키는 아래와 같습니다.
- text(필수) : 내용
- username : bot이름
- icon_url : 아이콘경로
- icon_emoji : bot의 아이콘을 이모티콘으로 사용할 때 사용함. icon_url 또는 icon_emoji 둘중 하나를 사용합니다.
- channel : 채널 Override

## Slack과 Github의 연결
- https://lazypic.slack.com/apps/A8GBNUWU8-github
- github apps 설치이후 github 채널에서 아래처럼 타이핑합니다.
```
/github subscribe lazypic/repositoryName
```

## Reference
- https://api.slack.com/tutorials/slack-apps-hello-world
- https://api.slack.com/apps
