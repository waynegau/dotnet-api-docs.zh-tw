### <a name="wcf-transport-security-supports-certificates-stored-using-cng"></a>WCF 傳輸安全性支援儲存使用 CNG 憑證

|   |   |
|---|---|
|詳細資料|目標.NET Framework 4.6.2 起應用程式，WCF 傳輸安全性會支援使用 Windows 密碼編譯程式庫 (CNG) 儲存的憑證。 這項支援僅限於具有公開金鑰的憑證，且指數長度不能超過 32 位元。 當應用程式的目標.NET Framework 4.6.2 時，這項功能預設為開啟。在舊版的.NET Framework 中，嘗試使用 X509 憑證與 CSG 金鑰儲存提供者擲回例外狀況。|
|建議|目標.NET Framework 4.6.1 和舊版，但在.NET Framework 4.6.2 執行的應用程式可啟用支援 CNG 憑證，將下列這一行加入<code>&lt;runtime&gt;</code>app.config 或 web.config 檔案區段：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableCngCertificates=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>這也可以用程式設計方式，以下列程式碼完成︰<pre><code class="language-cs">private const string DisableCngCertificates = @&quot;Switch.System.ServiceModel.DisableCngCertificate&quot;;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, false);&#13;&#10;</code></pre><pre><code class="language-vb">Const DisableCngCertificates As String = &quot;Switch.System.ServiceModel.DisableCngCertificates&quot;&#13;&#10;AppContext.SetSwitch(disableCngCertificates, False)&#13;&#10;</code></pre>請注意，由於這項變更，將不再執行任何倚賴使用 CNG 憑證嘗試起始安全通訊失敗的任何例外住況處理程式碼。|
|範圍|次要|
|版本|4.6.2|
|類型|正在重定目標|

