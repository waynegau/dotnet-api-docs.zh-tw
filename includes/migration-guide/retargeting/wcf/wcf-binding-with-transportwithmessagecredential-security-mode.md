### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>使用 TransportWithMessageCredential 安全性模式的 WCF 繫結

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.6.1 中，使用 TransportWithMessageCredential 安全性模式的 WCF 繫結可以設定為接收訊息的不帶正負號&quot;至&quot;標頭的非對稱安全性金鑰。根據預設，不帶正負號&quot;至&quot;標頭會繼續.NET 4.6.1 中遭到拒絕。 此外，他們只會接受如果 opts 進入作業使用 Switch.System.ServiceModel.AllowUnsignedToHeader 組態參數的這個新模式的應用程式。這是選擇性功能，因為它不會影響現有的應用程式的行為。|
|建議|由於這是可選擇加入的功能，因此不會影響現有應用程式的行為。 若要控制是否使用新的行為，請使用下列組態設定：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|透明|
|版本|4.6.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

