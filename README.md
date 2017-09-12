# test
測試上傳github

語法測試

This is a regular paragraph.
<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>
This is another regular paragraph.

# This is an H1

## This is an H2

###### This is an H6


# This is an H1 #

## This is an H2 ##

### This is an H3 ######



> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.



> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.


*   Red
*   Green
*   Blue
+   Red
+   Green
+   Blue
-   Red
-   Green
-   Blue
1.  Bird
2.  McHale
3.  Parish
<ol>
<li>Bird</li>
<li>McHale</li>
<li>Parish</li>
</ol>


This is a normal paragraph:

    This is a code block.



你可以在一行中用三個或以上的星號、減號、底線來建立一個分隔線，行內不能有其他東西。你也可以在星號中間插入空白。下面每種寫法都可以建立分隔線：

* * *

***

*****

- - -

---------------------------------------
區段元素

連結

Markdown支援兩種形式的連結語法：行內和參考兩種形式。

不管是哪一種，連結的文字都是用 [方括號] 來標記。

要建立一個行內形式的連結，只要在方塊括號後面馬上接著括號並插入網址連結即可，如果你還想要加上連結的title文字，只要在網址後面，用雙引號把title文字包起來即可，例如：

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.
會產生：

<p>This is <a href="http://example.com/" title="Title">
an example</a> inline link.</p>

<p><a href="http://example.net/">This link</a> has no
title attribute.</p>
如果你是要連結到同樣主機的資源，你可以使用相對路徑：

See my [About](/about/) page for details.
參考形式的連結使用另外一個方括號接在連結文字的括號後面，而在第二個方括號裡面要填入用以辨識連結的標籤：

This is [an example][id] reference-style link.
你也可以選擇性地在兩個方括號中間加上空白：

This is [an example] [id] reference-style link.
接著，在文件的任意處，你可以把這個標籤的連結內容定義出來：

[id]: http://example.com/  "Optional Title Here"
連結定義的形式為：

方括號，裡面輸入連結的辨識用標籤
接著一個冒號
接著一個以上的空白或tab
接著連結的網址
選擇性地接著title內容，可以用單引號、雙引號或是括弧包著
下面這三種連結的定義都是相同：

[foo]: http://example.com/  "Optional Title Here"
[foo]: http://example.com/  'Optional Title Here'
[foo]: http://example.com/  (Optional Title Here)
請注意：有一個已知的問題是Markdown.pl 1.0.1會忽略單引號包起來的連結title。

連結網址也可以用角括號包起來：

[id]: <http://example.com/>  "Optional Title Here"
你也可以把title屬性放到下一行，也可以加一些縮排，網址太長的話，這樣會比較好看：

[id]: http://example.com/longish/path/to/resource/here
    "Optional Title Here"
網址定義只有在產生連結的時候用到，並不會直接出現在文件之中。

連結辨識標籤可以有字母、數字、空白和標點符號，但是並不區分大小寫，因此下面兩個連結是一樣的：

[link text][a]
[link text][A]
預設的連結標籤功能讓你可以省略指定連結標籤，這種情形下，連結標籤和連結文字會視為相同，要用預設連結標籤只要在連結文字後面加上一個空的方括號，如果你要讓"Google"連結到google.com，你可以簡化成：

[Google][]
然後定義連結內容：

[Google]: http://google.com/
由於連結文字可能包含空白，所以這種簡化的標籤內也可以包含多個文字：

Visit [Daring Fireball][] for more information.
然後接著定義連結：

[Daring Fireball]: http://daringfireball.net/
連結的定義可以放在文件中的任何一個地方，我比較偏好直接放在連結出現段落的後面，你也可以把它放在文件最後面，就像是註解一樣。

下面是一個參考式連結的範例：

I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"
如果改成用連結名稱的方式寫：

I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"
上面兩種寫法都會產生下面的HTML。

<p>I get 10 times more traffic from <a href="http://google.com/"
title="Google">Google</a> than from
<a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>
下面是用行內形式寫的同樣一段內容的Markdown文件，提供作為比較之用：

I get 10 times more traffic from [Google](http://google.com/ "Google")
than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
[MSN](http://search.msn.com/ "MSN Search").
參考式的連結其實重點不在於它比較好寫，而是它比較好讀，比較一下上面的範例，使用參考式的文章本身只有81個字元，但是用行內形式的連結卻會增加到176個字元，如果是用純HTML格式來寫，會有234個字元，在HTML格式中，標籤比文字還要多。

使用Markdown的參考式連結，可以讓文件更像是瀏覽器最後產生的結果，讓你可以把一些標記相關的資訊移到段落文字之外，你就可以增加連結而不讓文章的閱讀感覺被打斷。

強調

Markdown使用星號（*）和底線（_）作為標記強調字詞的符號，被*或_包圍的字詞會被轉成用<em>標籤包圍，用兩個*或_包起來的話，則會被轉成<strong>，例如：

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__
會轉成：

<em>single asterisks</em>

<em>single underscores</em>

<strong>double asterisks</strong>

<strong>double underscores</strong>
你可以隨便用你喜歡的樣式，唯一的限制是，你用什麼符號開啟標籤，就要用什麼符號結束。

強調也可以直接插在文字中間：

un*frigging*believable
但是如果你的 * 和 _ 兩邊都有空白的話，它們就只會被當成普通的符號。

如果要在文字前後直接插入普通的星號或底線，你可以用反斜線：

\*this text is surrounded by literal asterisks\*
程式碼

如果要標記一小段行內程式碼，你可以用反引號

Use the `printf()` function.
會產生：

<p>Use the <code>printf()</code> function.</p>
如果要在程式碼區段內插入反引號，你可以用多個反引號來開啟和結束程式碼區段：

``There is a literal backtick (`) here.``
這段語法會產生：

<p><code>There is a literal backtick (`) here.</code></p>
程式碼區段的起始和結束端都可以放入一個空白，起始端後面一個，結束端前面一個，這樣你就可以在區段的一開始就插入反引號：

A single backtick in a code span: `` ` ``

A backtick-delimited string in a code span: `` `foo` ``
會產生：

<p>A single backtick in a code span: <code>`</code></p>

<p>A backtick-delimited string in a code span: <code>`foo`</code></p>
在程式碼區段內，&和角括號都會被轉成HTML實體，這樣會比較容易插入HTML原始碼，Markdown會把下面這段：

Please don't use any `<blink>` tags.
轉為：

<p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>
你也可以這樣寫：

`&#8212;` is the decimal-encoded equivalent of `&mdash;`.
以產生：

<p><code>&amp;#8212;</code> is the decimal-encoded
equivalent of <code>&amp;mdash;</code>.</p>
圖片

很明顯地，要在純文字應用中設計一個「自然」的語法來插入圖片是有一定難度的。

Markdown使用一種和連結很相似的語法來標記圖片，同樣也允許兩種樣式：行內和參考。

行內圖片的語法看起來像是：

![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")
詳細敘述如下：

一個驚嘆號!
接著一個方括號，裡面放上圖片的替代文字
接著一個普通括號，裡面放上圖片的網址，最後還可以用引號包住並加上 選擇性的'title'文字。
參考式的圖片語法則長得像這樣：

![Alt text][id]
「id」是圖片參考的名稱，圖片參考的定義方式則和連結參考一樣：

[id]: url/to/image  "Optional title attribute"
到目前為止， Markdown還沒有辦法指定圖片的寬高，如果你需要的話，你可以使用普通的<img>標籤。

其他

自動連結

Markdown支援比較簡短的自動連結形式來處理網址和電子郵件信箱，只要是用角括號包起來，Markdown就會自動把它轉成連結，連結的文字就和連結位置一樣，例如：

<http://example.com/>
Markdown會轉為：

<a href="http://example.com/">http://example.com/</a>
自動的郵件連結也很類似，只是Markdown會先做一個編碼轉換的過程，把文字字元轉成16進位碼的HTML實體，這樣的格式可以混淆一些不好的信箱地址收集機器人，例如：

<address@example.com>
Markdown會轉成：

<a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
&#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
&#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>
在瀏覽器裡面，這段字串會變成一個可以點擊的「address@example.com」連結。

（這種作法雖然可以混淆不少的機器人，但並無法全部擋下來，不過這樣也比什麼都不做好些。無論如何，公開你的信箱終究會引來廣告信件的。）

跳脫字元

Markdown可以利用反斜線來插入一些在語法中有其他意義的符號，例如：如果你想要用星號加在文字旁邊的方式來做出強調效果（但不用<em>標籤），你可以在星號的前面加上反斜線：

\*literal asterisks\*
Markdown支援在下面這些符號前面加上反斜線來幫助插入普通的符號：

\   反斜線
`   反引號
*   星號
_   底線
{}  大括號
[]  方括號
()  括號
#   井字號
+   加號
-   減號
.   英文句點
!   驚嘆號
