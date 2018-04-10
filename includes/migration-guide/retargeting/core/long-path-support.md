### <a name="long-path-support"></a>長路徑支援

|   |   |
|---|---|
|詳細資料|從應用程式開始支援.NET Framework 4.6.2，長的路徑 (最多 32 千個字元），該目標和 260 個字元 (或<code>MAX_PATH</code>) 路徑長度限制已經移除。針對以.NET Framework 4.6.2 目標來重新編譯的應用程式，程式碼路徑先前擲回<xref:System.IO.PathTooLongException?displayProperty=name>因為路徑超過 260 個字元現在將會擲回<xref:System.IO.PathTooLongException?displayProperty=name>只有在下列情況下：<ul><li>路徑的長度大於<xref:System.Int16.MaxValue>(32,767) 的字元。</li><li>作業系統傳回 <code>COR_E_PATHTOOLONG</code> 或其對應項。</li></ul>針對以.NET Framework 4.6.1 和更早版本為目標的應用程式，執行階段自動就會擲回<xref:System.IO.PathTooLongException?displayProperty=name>每當路徑超過 260 個字元。|
|建議|針對.NET Framework 4.6.2 目標的應用程式，您可以選擇退出冗長的路徑支援如果不想要新增至以下<code>&lt;runtime&gt;</code>區段您<code>app.config</code>檔案：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>目標的應用程式的舊版.NET Framework 但在.NET Framework 4.6.2 上執行或更新版本中，您也可以選擇長路徑支援新增至以下<code>&lt;runtime&gt;</code>區段您<code>app.config</code>檔案：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.6.2|
|類型|正在重定目標|

