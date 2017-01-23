# Netease Cloud Music API
Set the request header：
```bash
Accept:*/*,
Accept-Encoding:gzip, deflate,
Accept-Language:zh-CN,zh;q=0.8,en;q=0.6,
Connection:keep-alive,
Content-Type:application/x-www-form-urlencoded,
Cookie:appver=1.5.0.75771,
Host:music.163.com,
Origin:http://music.163.com,
Referer:http://music.163.com,
User-Agent:Mozilla/5.0 (Macintosh; Intel Mac OS X, 10_12_2) AppleWebKit/537.36 (KHTML, like Gecko), Chrome/55.0.2883.95 Safari/537.36,
```
1.User playlist：
```bash
# uid: user id; offset:0; limit:100; method:get;
http://music.163.com/api/user/playlist/?offset=0&limit=100&uid=
```
2.Recommend playlist:
```bash
# csrf: cookie.'__csrf';method: post;params: ;encSecKey : ;
http://music.163.com/weapi/v1/discovery/recommend/songs?csrf_token=csrf
```
3.User FM：
```bash
# default return 3 song;
http://music.163.com/api/radio/get
```
4.Search：
```bash
#method:post
#s:keywords
#type:song(1) singer(100) album(1000) user(1002)
#offset:0
#total:true
#limit:100（userDefined）
http://music.163.com/api/search/get
```
5.New albums
```bash
#area:ALL
#offset:0
#total:true
#limit:1（userDefined）
http://music.163.com/api/album/new?area=ALL&offset=0&total=true&limit=1
```
6.Top playlists
```bash
#cat:type （for example：“全部”,"日语"...）
#order:hot
#offset:0
#total:true
#limit:1（userDefined）
http://music.163.com/api/playlist/list?cat=&order=&offset=&total=&limit=
```
7.Playlist detail
```bash
#id:  playlistId
# '云音乐新歌榜', 3779629
# '云音乐热歌榜', 3778678
# '网易原创歌曲榜', 2884035
# '云音乐飙升榜', 19723756
# '云音乐电音榜', 10520166
# 'UK排行榜周榜', 180106
# '美国Billboard周榜', 60198
# 'KTV嗨榜', 21845217
# 'iTunes榜', 11641012
# 'Hit FM Top榜', 120001
# '日本Oricon周榜', 60131
# '韩国Melon排行榜周榜', 3733003
# '韩国Mnet排行榜周榜', 60255
# '韩国Melon原声周榜', '6772709
# '中国TOP排行榜(港台榜)', 112504
# '中国TOP排行榜(内地榜)', 64016
# '香港电台中文歌曲龙虎榜', 10169002
# '华语金曲榜', 4395559
# '中国嘻哈榜', 1899724
# '法国 NRJ EuroHot 30周榜', 27135204
# '台湾Hito排行榜', 112463
# 'Beatport全球电子舞曲榜', 3812895
http://music.163.com/api/playlist/detail?id=
```
8.Top artists
```bash
#offset:0
#total:false
#limit:1（userDefined）
http://music.163.com/api/artist/top?offset=&total=&limit=
```
9.Artists
```bash
#id:artistId
http://music.163.com/api/artist/id
```
10.Album
```bash
#id:albumId
http://music.163.com/api/album/id
```
11.Song comments
```bash
#id:songId
#offset:0
#total:false
#limit:1（userDefined）
http://music.163.com/api/v1/resource/comments/R_SO_4_id/?rid=R_SO_4_id&\offset=&total=&limit=
```
12.Song detail
```bash
#id:songId
http://music.163.com/api/song/detail?ids=[id]
```
13.Song url detail
```bash
#id:songId
http://music.163.com/api/song/detail/?id=&ids=[id]
```
14.Song lyric
```bash
#id:songId
http://music.163.com/api/song/lyric?os=osx&id=&lv=-1&kv=-1&tv=-1
```
15.MV
```bash
#id:mvId
http://music.163.com/api/mv/detail?id=&type=mp4
```
# License
[MIT]()
