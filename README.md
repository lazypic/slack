# Slack
Lazypic은 채팅 솔루션으로 Slack을 사용합니다.

채널 : https://lazypic.slack.com

Slack자체로도 훌륭하지만 조금더 커스터마이징 하기위해서
그룹을 위해서 셋팅하는 방법을 다루는 리포지터를 추가합니다.

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

## Reference
- https://api.slack.com/tutorials/slack-apps-hello-world
- https://api.slack.com/apps
