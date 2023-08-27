FORMAT: 1A
HOST: https://news-api.entry.nintendo.co.jp

# MyNintendo API Blueprint

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
