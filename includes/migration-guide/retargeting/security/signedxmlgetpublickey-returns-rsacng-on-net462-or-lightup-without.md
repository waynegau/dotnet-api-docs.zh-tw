### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey RSACng net462 （或 lightup） 傳回不含重定目標變更

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.6.2，所傳回的物件具象型別<xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType>方法 （不含突變） 從變更的 CryptoServiceProvider 實作 Cng 實作。 這是因為使用的實作變更<code>certificate.PublicKey.Key</code>使用內部<code>certificate.GetAnyPublicKey</code>其轉送給<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>。|
|建議|從.NET Framework 4.7.1 上執行的應用程式開始，您可以使用.NET Framework 4.6.1 中的預設使用的 CryptoServiceProvider 實作，並新增下列設定的較早版本切換至[執行階段](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)您應用程式組態檔區段：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.6.2|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

