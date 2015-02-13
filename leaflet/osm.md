#OpenStreetMap小記

開放街圖（英語：OpenStreetMap，縮寫：OSM）是一個建構自由內容之網上地圖協作計劃，目標是創造一個內容自由且能讓所有人編輯的世界地圖，並且讓一般便宜的行動裝置有方便的導航方案。 by wiki

[osm網站](http://www.openstreetmap.org/)

##概略

[swith to osm](http://switch2osm.org/serving-tiles/building-a-tile-server-from-packages)

- 開放的地圖，任何人都可以編輯修改，所以地圖更新的速率是靠當地人的參與度而定。
- 沒有導航，沒有商家資訊，沒有街景，只有地圖。
- 因為OSM只有底圖的關係，要顯示或是增加東西上去只能藉openlayer leaflet這類圖層容器。

##底圖(tile)

- OSM的底圖是畫死的，沒辦法用api開關顯示街道還是建築物
- [tile server列表](http://wiki.openstreetmap.org/wiki/Tile_servers)，當然還有很多別的tile供應商沒有寫上去，像是mapbox。
- [Tilemill地圖編輯器](https://www.mapbox.com/tilemill/)，讓你製作自己的til，不過要自己host server。
- [Manually building a tile server (12.04)](http://switch2osm.org/serving-tiles/manually-building-a-tile-server-12-04/)


##心得

[世界為什麼需要 OpenStreetMap？](http://www.techbang.com/posts/16464-power-on-the-map-the-world-why-openstreetmap)
基本上OSM要跟google map拼是不可能的，社群活躍跟地圖修正的速度都看不到車尾燈，方便性也差一大截，不過基於開放的概念，如果你不想要google推薦你怎麼走，或是需要一個漂亮的客製化地圖，OSM會是你的好選擇。
