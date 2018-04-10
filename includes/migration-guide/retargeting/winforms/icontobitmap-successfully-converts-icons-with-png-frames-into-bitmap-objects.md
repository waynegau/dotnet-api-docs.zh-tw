### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap 已成功將具有 PNG 畫面格圖示轉換為點陣圖物件

|   |   |
|---|---|
|詳細資料|從目標為.NET Framework 4.6 中，應用程式開始<xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType>方法已成功將具有 PNG 畫面格圖示轉換為點陣圖物件。應用程式中的目標.NET Framework 4.5.2 及更新版本、<xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType>方法會擲回<xref:System.ArgumentOutOfRangeException>如果圖示物件具有 PNG 畫面格的例外狀況。這項變更會影響重新撰寫.NET Framework 4.6 為目標，以及實作特殊處理的應用程式<xref:System.ArgumentOutOfRangeException>圖示物件具有 PNG 畫面格時，會擲回。 以 .NET Framework 4.6 執行時，轉換會成功，且不再擲回 <xref:System.ArgumentOutOfRangeException> ，因此不會再叫用例外狀況處理常式。|
|建議|如果不需要這個行為，您可以藉由新增下列項目加入保留舊有行為<code>&lt;runtime&gt;</code>app.config 檔的區段：<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>如果 app.config 檔已經包含<code>AppContextSwitchOverrides</code>項目，新值應該合併 value 屬性的值如下：<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.6|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

