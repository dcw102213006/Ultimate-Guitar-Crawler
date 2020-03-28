`Ultimate_crawl_artistname`
  + Website:[Ultimate Guitar](https://www.ultimate-guitar.com/)
  + Target:
    + Artist name
    + Artist Url
    
Description:
這隻爬取網站上Pop music的歌手名字與URL下來
之後就可以針對每個歌手的URL把所有譜抓下來

___ 

`Ultimate_craw`
  + Source:MongoDB:Ultimate_Guitar_Artist
  + Target: Html of Tabs
  + Save To:MongoDB:

Description:從MongoDB取出流行樂歌手名稱與URL資料，爬取每一位歌手的吉他譜Html

例如:
+ 想抓beatles的所有吉他譜
+ 請求URL:https://www.ultimate-guitar.com/artist/the_beatles_1916
+ 選擇type=chord的吉他譜

透過歌手URL把每個歌手的所有吉他譜頁面的Html抓下來，存在Mongo DB(先抓HTML存Mongo，之後取出來解析)
___


`Ultimate_craw_TabHtmlParse`

Description
這支把爬下來的HTML從MongoDB撈出來並解析HTML以取得資訊(歌手、歌名、歌曲和弦、曲譜Rating等等)並存回MongoDB

