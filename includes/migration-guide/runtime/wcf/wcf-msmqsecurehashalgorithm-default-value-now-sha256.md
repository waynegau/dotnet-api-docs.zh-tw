### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>WCF MsmqSecureHashAlgorithm 預設值現在是 SHA256

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.7.1 開始，預設的訊息簽章在 WCF 中的 Msmq 訊息的演算法是 SHA256。 在.NET Framework 4.7 和更早版本中，預設的訊息簽章演算法是 SHA1。|
|建議|如果在.NET Framework 4.7.1 上執行這項變更的相容性問題或更新版本中，您可以退出變更將下列這一行加入<code>&lt;runtime&gt;</code>app.config 檔的區段：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7.1|
|類型|執行階段|

