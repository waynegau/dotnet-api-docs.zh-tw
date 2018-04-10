### <a name="serialport-background-thread-exceptions"></a>SerialPort 背景執行緒例外狀況

|   |   |
|---|---|
|詳細資料|背景執行緒與建立<xref:System.IO.Ports.SerialPort>資料流不會再終止處理序時 OS 的例外狀況。在以.NET Framework 4.7 和更早版本為目標的應用程式，以建立在背景執行緒上擲回例外狀況的作業系統時，已終止處理程序<xref:System.IO.Ports.SerialPort>資料流。應用程式中，目標為.NET Framework 4.7.1 或更新版本，背景執行緒等候 OS 事件與作用中的序列通訊埠相關，可能會損毀，請在某些情況下，例如突然移除序列連接埠。|
|建議|針對.NET Framework 4.7.1 為目標的應用程式，您可以選擇退出例外狀況處理，如果不想要新增至以下<code>&lt;runtime&gt;</code>區段您<code>app.config</code>檔案：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>目標的應用程式的舊版.NET Framework 但在.NET Framework 4.7.1 上執行或更新版本中，您也可以選擇新增下列命令來處理的例外狀況<code>&lt;runtime&gt;</code>區段您<code>app.config</code>檔案：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

