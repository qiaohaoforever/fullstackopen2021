## 练习

###  HTML
通过阅读 Mozilla 的[HTML tutorial](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)来回顾 HTML 的基础知识。

### CSS
通过阅读 Mozilla 的[CSS tutorial](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics).来回顾 CSS 的基础知识。

### HTML forms
通过阅读 Mozilla 的 [Your first form](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form)教程了解 HTML 表单的基础知识。

### 时序图
页面打开 https://studies.cs.helsinki.fi/exampleapp/notes 时引起的事件链被描述为一个时序图

该图是使用 websequencediagrams 服务绘制的，如下所示:
```
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
server-->browser: HTML-code
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
server-->browser: main.js

note over browser:
browser starts executing js-code
that requests JSON data from server
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{ content: "HTML is easy", date: "2019-05-23" }, ...]

note over browser:
browser executes the event handler
that renders notes to display
end note
```
![https://studies.cs.helsinki.fi/exampleapp/notes](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=dGl0bGUgd2hlbiBjbGljayB1cmwKCmJyb3dzZXItPnNlcnZlcjogSFRUUCBHRVQgaHR0cHM6Ly9zdHVkaWVzLmNzLmhlbHNpbmtpLmZpL2V4YW1wbGVhcHAvbm90ZXMKADsGLS0-AEwHOiBIVE1MLWNvZGUAIUVtYWluLmNzAFUUABIJAB9JagBOGWpzCgpub3RlIG92ZXIgAIFkCACCQAggc3RhcnRzIGV4ZWN1dGluZyBqcwCBfQZ0aGF0IHJlcXVlc3RzIEpTT04gZGF0YSBmcm9tIACCdwYKZW5kIG5vdGUAglFGZGF0YS5qc29uAIMIE1t7IGNvbnRlbnQ6ICJIVE1MIGlzIGVhc3kiLCBkYXRlOiAiMjAxOS0wNS0yMyIgfSwgLi4uXQCBXR0AgW0GZXMgdGhlIGV2ZW50IGhhbmRsZXIAgXQIbmRlcnMAgVwFcyB0byBkaXNwbGF5AIFsCg&s=default)

#### Single page app
创建一个图表，描述用户在进入 https://studies.cs.helsinki.fi/exampleapp/spa 这个 Note 应用的单页版本的情况。
```
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa
server-->browser: HTML-code
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa.js
server-->browser: main.js

note over browser:
browser starts executing js-code
that requests JSON data from server
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{ content: "HTML is easy", date: "2019-05-23" }, ...]

note over browser:
browser executes the event handler
that renders notes to display
end note
```
![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=dGl0bGUgd2hlbiBjbGljayB1cmwKCmJyb3dzZXItPnNlcnZlcjogSFRUUCBHRVQgaHR0cHM6Ly9zdHVkaWVzLmNzLmhlbHNpbmtpLmZpL2V4YW1wbGVhcHAvc3BhCgA5Bi0tPgBKBzogSFRNTC1jb2RlAB9FbWFpbi5jc3MAVhMAEgkAgQVHLmoATRlqcwoKbm90ZSBvdmVyIACBYwgAgj0IIHN0YXJ0cyBleGVjdXRpbmcganMAgXwGdGhhdCByZXF1ZXN0cyBKU09OIGRhdGEgZnJvbSAAgnQGCmVuZCBub3RlAIJORmRhdGEuanNvbgCDBxNbeyBjb250ZW50OiAiSFRNTCBpcyBlYXN5IiwgZGF0ZTogIjIwMTktMDUtMjMiIH0sIC4uLl0AgV0dAIFtBmVzIHRoZSBldmVudCBoYW5kbGVyAIF0CG5kZXJzAIFcBXMgdG8gZGlzcGxheQCBbAo&s=default)


#### New note
创建一个图表描述如下情况，用户使用应用的 SPA 版本创建一个新的Note 。
```
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa
server-->browser: HTML-code
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa.js
server-->browser: main.js

note over browser:
browser starts executing js-code
that requests JSON data from server
end note

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note { content: "HTML is easy", date: "2019-05-23" }

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{ content: "HTML is easy", date: "2019-05-23" }, ...]

note over browser:
browser executes the event handler
that renders notes to display
end note
```
![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=dGl0bGUgd2hlbiBjbGljayB1cmwKCmJyb3dzZXItPnNlcnZlcjogSFRUUCBHRVQgaHR0cHM6Ly9zdHVkaWVzLmNzLmhlbHNpbmtpLmZpL2V4YW1wbGVhcHAvc3BhCgA5Bi0tPgBKBzogSFRNTC1jb2RlAB9FbWFpbi5jc3MAVhMAEgkAgQVHLmoATRlqcwoKbm90ZSBvdmVyIACBYwgAgj0IIHN0YXJ0cyBleGVjdXRpbmcganMAgXwGdGhhdCByZXF1ZXN0cyBKU09OIGRhdGEgZnJvbSAAgnQGCmVuZCBub3RlAIJ8GFBPUwCCaSxuZXdfAIEmBXsgY29udGVudDogIkhUTUwgaXMgZWFzeSIsIGRhdGU6ICIyMDE5LTA1LTIzIiB9AINNRmRhdGEuanNvbgCEBhNbAGMvLCAuLi5dAIJcHQCCbAZlcyB0aGUgZXZlbnQgaGFuZGxlcgCCcwhuZGVycwCCWwVzIHRvIGRpc3BsYXkAgmsK&s=default)