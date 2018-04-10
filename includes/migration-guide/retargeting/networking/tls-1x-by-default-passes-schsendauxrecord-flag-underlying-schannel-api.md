### <a name="tls-1x-by-default-passes-the-schsendauxrecord-flag-to-the-underlying-schannel-api"></a>TLS 1.x 依預設會將 SCH_SEND_AUX_RECORD 旗標傳遞至基礎的安全通道應用程式開發介面

|   |   |
|---|---|
|詳細資料|使用 TLS 時 1.x，.NET Framework 依賴基礎 Windows 安全通道 API。 從.NET Framework 4.6，開始[SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx)旗標的預設值傳遞至安全通道。 這會導致分割成兩個不同的記錄，做為單一位元組和第二個做為第一個要加密資料的安全通道<em>n</em>-1 個位元組。在罕見的情況下，這會中斷用戶端與假設資料所在的單一記錄中的現有伺服器之間的通訊。|
|建議|如果這項變更會中斷現有的伺服器的通訊，您可以停用傳送[SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx)旗標，並還原先前的行為，不將資料分割成個別的記錄中，加入下列參數來變更[ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)中[ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)您應用程式組態檔：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontEnableSchSendAuxRecord=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] 基於回溯相容性提供此設定。 否則不建議使用它。</blockquote> |
|範圍|Edge|
|版本|4.6|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

