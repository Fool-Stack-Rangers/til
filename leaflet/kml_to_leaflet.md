#leaflet地圖上使用kml顯示

<img src="http://i.imgur.com/VIFXzA6.png">

##[kml介紹](http://zh.wikipedia.org/wiki/KML)

因為用google map可能會遇到收費問題，為了怕麻煩選擇使用leaflet + osm<s>，結果更麻煩</s>。

##方式

因為leaflet本身不支援直接讀入kml，所以必須依賴其它外掛，在翻閱之後找到兩種可行方法

- [omnivore - mapbox](https://github.com/mapbox/leaflet-omnivore)
- [KML外掛 - Harry Wood](http://harrywood.co.uk/maps/examples/leaflet/kml.view.html)

##omnivore

[範例](https://www.mapbox.com/mapbox.js/example/v1.0.0/omnivore-custom-layer/)

簡單，好用，缺點是kml上去map時，kml裡面設定的style無法一起轉，如果不介意上去之後再調顏色，會是個首選，但是因為我覺得這個是一個必要的條件，所以放棄改用下一個。

##KML

[範例](http://bl.ocks.org/ramnathv/6562757)

使用也是相當容易，style設定也會跟著轉，但是因為本身是用extend的方式來加強原本feature的屬性，結果導致feature屬性無法紀錄name跟description，範例上面是用bindpopup解決。

因為我需要description的值來click觸發ajax，原本想直接改他的code，但他的寫法太過漂亮跟OOP以至於我看不懂，改了一天改不出結果所以放棄。

##Geojson

[kmltojson](https://github.com/mapbox/togeojson)
[範例](http://leafletjs.com/examples/geojson.html)

上面兩個都無法一次到位的情況下，找到了一個最奇怪的解法，先把kml轉成geojson在弄成 geojson layer，因為看到網路上有示範將kml的style漂亮的轉成geojson，想說這個應該就是最佳解了。

結果我的kml轉geojson時因為寫法不同，導致轉過去之後的geojson layer仍是無法正常顯示顏色，還是必須要靠自己寫的style（那不就跟第一個一樣？）。

##心得

花了一堆時間結果繞了一圈，因為一直很想要避免版權或是商業使用的問題...如果你想要用kml顯示地圖的話，乖乖使用google map 吧，付錢消災。用google map的好處就是你什麼都可以丟給他他什麼都吃，而且都可以很漂亮的顯示，但是像是leaflet或是openlayer這種opensource的容器，幾乎沒有辦法完美的表現，都需要花費許多心思微調。

不過我之後想花一點時間把第二個ＫＭＬ改寫一下...如果成功就是最佳解了！
