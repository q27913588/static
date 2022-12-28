curl --location --request POST 'http://localhost:8087/pushservice/member/register
' \
--header 'Content-Type: application/json' \
--data-raw '{
    "app_id": "whoAmI",
    "app_secret": "zsdluiawelkr5weraq1",
    "app": "test",
    "list": [
        {
            "memberId": "member01",
            "token": "dwC-fUf9SWWi4Yy8BA0fyO:APA91bE2CAe2J9ERZnnJ14LmSg-1YOWMEz2fTx4dN_7TadLSeDrqzZIX0xPGYLes05Eef7DwOhitTNiVeTIgg8Bmil403FgQYEqw9LFZ3Yq7mSSjaar4dotfriDZJmI4N-iKX4pU0bfi"
        }
    ]
}
'



curl --location --request POST 'http://localhost:8087/pushservice/member/push
' \
--header 'Content-Type: application/json' \
--data-raw '{
    "app_id": "whoAmI",
    "app_secret": "zsdluiawelkr5weraq1",
    "app": "test",
    "title": "title1",
    "message": "message1",
    "schedule": "2022/09/09 13:34:57",
    "broadcast": false,
    "memberIdList": [
        "member01"
    ]
}
'
