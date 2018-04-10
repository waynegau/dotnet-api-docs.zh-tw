### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase 不會傳播 OnStart 例外狀況

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.7 和更早版本中，在服務啟動時擲回例外狀況不會傳播至呼叫端的<xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>。從.NET Framework 4.7.1 為目標的應用程式開始，執行階段會傳播到的例外狀況<xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>無法啟動的服務。|
|建議|在服務啟動例外狀況，是否將傳播例外狀況。 這應該可以協助診斷服務無法啟動的情況。如果不需要這個行為，您可以新增以下選擇不使用<AppContextSwitchOverrides>元素<runtime>應用程式組態檔區段：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>如果您的應用程式的目標 4.7.1 比舊版，但您想要有這種行為，加入下列<AppContextSwitchOverrides>元素<runtime>應用程式組態檔區段：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

