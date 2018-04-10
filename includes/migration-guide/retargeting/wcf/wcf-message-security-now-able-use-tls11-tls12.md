### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>WCF 訊息安全性現在就可以使用 TLS1.1 和 TLS1.2

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.7 開始，客戶可以 TLS1.1 或 TLS1.2 中設定 WCF 訊息安全性，除了 SSL3.0 和 TLS1.0 透過應用程式組態設定。|
|建議|在.NET Framework 4.7 中，預設會停用 WCF 訊息安全性中 TLS1.1 和 TLS1.2 的支援。 您可以加入下列這一行來啟用<code>&lt;runtime&gt;</code>app.config 或 web.config 檔案區段：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.7|
|類型|正在重定目標|

