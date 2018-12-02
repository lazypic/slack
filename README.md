# Slack
Lazypic은 채팅 솔루션으로 Slack을 사용합니다.
Slack자체를 그대로 사용가능하지만 조금더 커스터마이징 하기위해서
셋팅하는 방법을 다루는 리포지터를 생성하였습니다.

## 방해금지모드 사용법
Slack을 사용하는 이유는 방해금지 시간을 자유롭게 설정할 수 있기 때문입니다.
취침시간, 휴식시간등 자유롭게 설정하고 사용하세요.

![slack_setting01](https://user-images.githubusercontent.com/1149996/49338806-974a5f00-f66a-11e8-8df2-7acd35f808da.png)

![slack_setting02](https://user-images.githubusercontent.com/1149996/49338807-974a5f00-f66a-11e8-86b0-8806efc7a829.png)

![slack_setting03](https://user-images.githubusercontent.com/1149996/49338809-974a5f00-f66a-11e8-8867-14f1989df591.png)


## 채널설정
관리자 설정페이지 : https://lazypic.slack.com/customize

## Apps 추가 및 Webhook 활성화
채팅 채널에 자동으로 메시지를 전송하기 위해서 사용합니다. webhook 토큰을 알고 싶다면 admin@lazypic.org로 메일주세요.

- https://api.slack.com/apps
- https://api.slack.com/apps/AEGKLE3T3/incoming-webhooks?success=1

```
$ curl -X POST -H 'Content-type: application/json' --data '{"text":"Hello, Slack!"}' https://hooks.slack.com/service/{token}/{token}/{token}
```

지원하는 data의 키는 아래와 같습니다.
- text(필수) : 내용
- username : bot이름
- icon_url : 아이콘경로
- icon_emoji : bot의 아이콘을 이모티콘으로 사용할 때 사용함. icon_url 또는 icon_emoji 둘중 하나를 사용합니다.
- channel : 채널 Override

## Slack <-> Github
- https://lazypic.slack.com/apps/A8GBNUWU8-github

## Reference
- https://api.slack.com/tutorials/slack-apps-hello-world
