##img tag在markdown轉成html之後會被包在p tag內

###起因：如果你有設定`<p>`的一些屬性，會連帶影響到`<img>`

###解法：無解

因為markdown spec指出

>A paragraph is simply one or more consecutive lines of text, separated by one or more blank lines.

我目前就是在前後在用div包起來，非常沒效率而且沒解決問題。

    <div> <img> </div>

僅此。