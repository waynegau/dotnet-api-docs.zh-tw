### <a name="certificate-eku-oid-validation"></a>憑證 EKU OID 驗證

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.6，開始<xref:System.Net.Security.SslStream>或<xref:System.Net.ServicePointManager>類別執行增強金鑰使用 (EKU) 物件識別碼 (OID) 驗證。 增強金鑰使用方法 (EKU) 延伸模組是物件識別碼 (Oid)，以指出應用程式使用金鑰的集合。 為 EKU OID 驗證會使用遠端憑證回呼，以確保遠端憑證有正確的 Oid 用於預定的目的。|
|建議|如果不需要這項變更，您可以加入停用憑證驗證為 EKU OID 下切換到[ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)中[ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)的程式應用程式組態檔：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] 基於回溯相容性提供此設定。 否則不建議使用它。</blockquote> |
|範圍|次要|
|版本|4.6|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

