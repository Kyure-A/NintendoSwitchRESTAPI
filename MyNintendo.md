FORMAT: 1A
HOST: https://news-api.entry.nintendo.co.jp

# MyNintendo API Blueprint

## Played Game List [/api/v1.1/users/me/play_histories]
### Get Played Game List [GET]
The `service_id_token` might be response from [here](./NintendoAccountBlueprint.md#service-token-connect100apitoken).
+ Request
  + Headers: 
  ```
  accept: */*
  accept-encoding: br;q=1.0, gzip;q=0.9, deflate;q=0.8
  user-agent: com.nintendo.znej/2.1.0 (iOS/16.6)
  accept-language: en-US;q=1.0, ja-JP;q=0.9
  authorization: Bearer ${service_id_token}
  ```
  + Body: none
 
+ Response 200
  + Body
    ```json
    {
    "hiddenTitleList": [],
    "lastUpdatedAt": "2023-08-27T21:28:38+09:00",
    "playHistories": [
        {
            "deviceType": "HAC", // Nintendo Switch
            "firstPlayedAt": "2023-01-12T04:48:12+09:00",
            "imageUrl": "https://atum-img-lp1.cdn.nintendo.net/i/c/1427016279c04de0b080b8dd26e209e0_256",
            "lastPlayedAt": "2023-08-09T16:11:06+09:00",
            "lastUpdatedAt": "2023-08-27T21:28:38+09:00",
            "titleId": "01008F6008C5E000",
            "titleName": "ポケットモンスター バイオレット",
            "totalPlayedDays": 47,
            "totalPlayedMinutes": 23827
        },
        {
            "deviceType": "HAC", // Nintendo Switch
            "firstPlayedAt": "2023-01-09T22:19:48+09:00",
            "imageUrl": "https://atum-img-lp1.cdn.nintendo.net/i/c/1adfe782967548c99659c27c9a3bca56_256",
            "lastPlayedAt": "2023-08-05T23:08:02+09:00",
            "lastUpdatedAt": "2023-08-27T21:28:38+09:00",
            "titleId": "01006A800016E000",
            "titleName": "大乱闘スマッシュブラザーズ SPECIAL",
            "totalPlayedDays": 13,
            "totalPlayedMinutes": 4966
        },
        {
            "deviceType": "CTR", // Nintendo 3DS
            "firstPlayedAt": "2014-11-21T00:00:00+09:00",
            "imageUrl": "https://idbe-img-lp1.cdn.nintendo.net/3ds/c786ab5bc6abb9bbed66b20a5f1d5ca6.png",
            "lastPlayedAt": "2016-10-31T00:00:00+09:00",
            "lastUpdatedAt": "2020-02-08T08:42:45+09:00",
            "titleId": "000400000011C400",
            "titleName": "ポケットモンスター オメガルビー",
            "totalPlayedDays": 79,
            "totalPlayedMinutes": 7072
        },
    ],
    "recentPlayHistories": [
        {
            "dailyPlayHistories": [
                {
                    "imageUrl": "https://atum-img-lp1.cdn.nintendo.net/i/c/1427016279c04de0b080b8dd26e209e0_256",
                    "titleId": "01008F6008C5E000",
                    "titleName": "ポケットモンスター バイオレット",
                    "totalPlayedMinutes": 9
                }
            ],
            "playedDate": "2023-08-09T00:00:00+09:00"
        }
    ]
    }
    ```
  
## Game Play Histories [/api/v1/users/me/play_histories/game_titles/${game_id_here}]
### Get Game Play Histories [GET]
The `service_token_code` might be response from [here](./NintendoAccountBlueprint.md#service-token-connect100apitoken).
+ Request
  + Headers:
    ```
    accept: */* 
    accept-encoding: br;q=1.0, gzip;q=0.9, deflate;q=0.8
    user-agent: com.nintendo.znej/2.1.0 (iOS/16.6)
    accept-language: en-US;q=1.0, ja-JP;q=0.9
    authorization: Bearer ${service_token_code}
    ```
  + Body
    ```
    limit:  16
    offset: 16
    ```

+ Response 200
  + Body
    ```json
    {
    "deviceType": "HAC",
    "firstPlayedAt": "2023-01-12T04:48:12+09:00",
    "imageUrl": "",
    "lastPlayedAt": "2023-08-09T16:11:06+09:00",
    "lastUpdatedAt": "2023-08-27T21:01:18+09:00",
    "playedDays": [
        {
            "minutesPlayed": 1264,
            "playedDate": "2023-03-11T09:00:00+09:00"
        },
        {
            "minutesPlayed": 1475,
            "playedDate": "2023-03-10T09:00:00+09:00"
        },
        {
            "minutesPlayed": 688,
            "playedDate": "2023-03-09T09:00:00+09:00"
        },
        {
            "minutesPlayed": 4828,
            "playedDate": "2023-03-04T09:00:00+09:00"
        },
        {
            "minutesPlayed": 138,
            "playedDate": "2023-03-02T09:00:00+09:00"
        },
        {
            "minutesPlayed": 167,
            "playedDate": "2023-03-01T09:00:00+09:00"
        },
        {
            "minutesPlayed": 43,
            "playedDate": "2023-02-28T09:00:00+09:00"
        },
        {
            "minutesPlayed": 97,
            "playedDate": "2023-02-20T09:00:00+09:00"
        },
        {
            "minutesPlayed": 116,
            "playedDate": "2023-02-19T09:00:00+09:00"
        },
        {
            "minutesPlayed": 268,
            "playedDate": "2023-02-18T09:00:00+09:00"
        },
        {
            "minutesPlayed": 126,
            "playedDate": "2023-02-17T09:00:00+09:00"
        },
        {
            "minutesPlayed": 90,
            "playedDate": "2023-02-16T09:00:00+09:00"
        },
        {
            "minutesPlayed": 14,
            "playedDate": "2023-02-11T09:00:00+09:00"
        },
        {
            "minutesPlayed": 59,
            "playedDate": "2023-02-10T09:00:00+09:00"
        },
        {
            "minutesPlayed": 84,
            "playedDate": "2023-02-08T09:00:00+09:00"
        },
        {
            "minutesPlayed": 2,
            "playedDate": "2023-02-07T09:00:00+09:00"
        }
    ],
    "playedDaysOffset": 16,
    "titleId": "01008F6008C5E000",
    "titleName": "",
    "totalPlayedDays": 47,
    "totalPlayedMinutes": 23827
    }
    ```
titleId;  `01008F6008C5E000` is Pokemon Violet.
My Nintendo app might interprete title id into game title and game image.
