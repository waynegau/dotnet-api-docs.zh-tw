### <a name="throttle-concurrent-requests-per-session"></a>每一個工作階段的節流閥並行要求數目

|   |   |
|---|---|
|詳細資料|.NET Framework 4.6.2 中更早版本，ASP.NET，循序執行使用相同的 Sessionid 的要求，ASP.NET 一律會透過 cookie Sessionid 發出預設。 如果頁面會花很長的時間來回應，它將會大幅降低伺服器效能，只要在瀏覽器上按 F5。 在修正，我們加入了計數器來追蹤要求排入佇列，並終止要求時超過指定的限制。 預設值為 50。 如果達到限制時，警告將會記錄到事件記錄及 HTTP 500 回應可能會在 IIS 記錄檔中記錄中。|
|建議|若要還原舊行為，您可以將下列設定加入您的 web.config 檔案以選擇退出新行為。<pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.7|
|類型|正在重定目標|

