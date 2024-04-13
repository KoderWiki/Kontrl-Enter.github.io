---
layout: post
title: LOLEX Patch Notes
tags: [Web Develop, League of Legends, LOLEX]
feature-img: "assets/img/0.post/2024-04-13/header2.png"
thumbnail: "assets/img/0.post/2024-04-13/header.png"
categories: LOLEX
---

" This patch is fist patch in [**LOLEX**](http://ko-web.com/lolex). This patch is not added new fuction but **fixed a fatal BUGs**. "

For more information on **LOLEX**, Please click [**here**](https://koderwiki.github.io/lolex/2024/02/15/LOLEX-Release.html)! <br>

## [BUG.1] match-v5 returns meaningless data 

We've found that **some of match historys didn't recieved data properly**. After looking at the cause, we can find out that **the cause was RIOT API**.

```json
"info": {
        "endOfGameResult": "Abort_Unexpected",
        "frameInterval": 0,
        "frames": [
            {
                "events": [
                    {
                        "gameId": 6834713231,
                        "realTimestamp": 1709066369872,
                        "timestamp": 0,
                        "type": "GAME_END",
                        "winningTeam": 0
                    }
                ],
                "participantFrames": null,
                "timestamp": 0
            }
        ],
        "gameId": 0,
        "participants": []
    }
```
For what reason, Riot API sent data that didn't contain anything, so we can't recognize this. So we solved this problem by making an exception of error. But inevitably, **we can't confirm match records of the error**.

![image](https://github.com/KoderWiki/koderwiki.github.io/assets/153072257/95ccb3d1-e534-4d59-9dd7-7160071ed63f)

## [BUG.2] Changed structure of SUMMONER-V4

We've found that Summoner's name is inaccurate. It because, structure of SUMMONER-V4 is changed.

```python
    puuid = id_data['puuid']
    name_url = 'https://kr.api.riotgames.com/lol/summoner/v4/summoners/by-puuid/{}?api_key={}'.format(puuid,apikey)
    summoner_info = get_json(name_url)
    lol_name = name # Modified
    encrypted_id = summoner_info['id']
    profile_id = summoner_info['profileIconId']
    summoner_level = summoner_info['summonerLevel']
```

We solved this problem by receiving another variable.




























