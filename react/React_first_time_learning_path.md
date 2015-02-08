React 學習資源：
==
[awesome react](https://github.com/enaqx/awesome-react)


My learning path:
=

## 1. [官網的React教學](http://facebook.github.io/react/docs/tutorial.html)

## 2. [Why React?](http://facebook.github.io/react/docs/why-react.html)

### simple

當資料來源被更動的時候，畫面自動更新

當你想要改變資料的時候，react概念上像是按了**refresh** button，只更新資料改變的部分（不是雙向綁定，不會自動更新）

### Resuable
It's all about building component.

### Why did we build React? [source](http://facebook.github.io/react/blog/2013/06/05/why-react.html)

**React isn't an MVC framework.**


**React doesn't use templates.**

可以使用javascript製作markup，在大型應用程式中非常重要

不是view導向，而是component導向

邏輯與ui是抽不開的，不如將它封裝

避免string concatenation， eg: "I'm" + name + "."
避免更多的XSS議題，

### Reactive updates are dead simple.
第一次initialize的時候，react便會呼叫`render`，回傳一個關於view的輕量型描述(representation)，當資料改變時，`render`會再次被呼叫，這次會比對與上一次的描述，有哪些地方不同，計算怎麼樣可以更新最少的dom，才產生新的描述，再render到畫面上。

## 3. 蒐集各種React觀念文章

### [Rethinking Best Practices](http://www.slideshare.net/floydophone/react-preso-v2)

- Component, not template
- Re-render, don't mutate
- Virtual DOM let DOM operation simple and faster.

### [reusable-components](http://facebook.github.io/react/docs/reusable-components.html)

官方關於components的spec的簡短介紹

- prop validator
- prop shortcut
- default props
- mixins

## 4. 實作

### [follow up to build a memory game(改進版)](http://blog.krawaller.se/posts/a-react-js-case-study-follow-up/)

padding...

React Rails
=
[reactjs-and-rails](http://rny.io/rails/react/2014/07/31/reactjs-and-rails.html):
官方的範例，加上背後用rails當作backend

[rails-and-react-ii-a-real-use-case](http://codeloveandboards.com/blog/2014/09/10/rails-and-react-ii-a-real-use-case/)
完整的react + rails範例

## Gems must take a look
- react-rails
- sprockets-coffee-react


心得
=
用三隻小豬中的蓋草屋、木屋與磚屋舉例的話，當應用程式在轉換狀態的過程，可以類比為從草屋改建成木屋，木屋改建成磚屋，如果用以前jQuery單純操作DOM的方式build應用程式的話，就像是草屋改建成木屋的時候，必須要先把茅草從房子上拿下來，再把木頭運過來，然後把木頭一根根排上去，從木屋改建成磚屋時，一樣要去想如何改建，必須重新定義改建的方式(邏輯)，不過react有不一樣的思考方式，他比較像是，你先定義三種不同房子中相同的架構，像是要有一個屋頂，四根柱子、四面牆，定義好之後只需要建造一次，之後要草屋就把茅草貼上去，要木屋就把木屋擺上去，磚屋就把磚頭放上去，不同的狀態，只需要一套同樣處理事務的邏輯（這邊是把材料放上去），當你可以少寫code與減少生產各種邏輯的時候，自然可以減少bug。




