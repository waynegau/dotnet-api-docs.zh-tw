### <a name="default-signedxml-and-signedxms-algorithms-changed-to-sha256"></a>預設 SignedXML 和 SignedXMS 演算法變更為 SHA256

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.7 和舊版中，SignedXML 和 SignedCMS 預設為 SHA1 進行某些作業。從.NET Framework 4.7.1 開始，這些作業的預設會啟用 SHA256。 這項變更是必要的因為 SHA1 不再被視為是安全的方法。|
|建議|有兩個新內容參數的值來控制是否預設使用 SHA1 （不安全） 或 SHA256:<ul><li>Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms</li><li>Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms</li></ul>對於目標為.NET Framework 4.7.1 和更新版本，如果使用 SHA256 不適當時，您可以還原預設 SHA1 來藉由新增下列設定的應用程式切換至[執行階段](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)區段的應用程式組態檔案：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=true;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=true&quot; /&gt;&#13;&#10;</code></pre>對於目標為.NET Framework 4.7 和更早版本的應用程式，您可以選擇這項變更成加入至下列的組態參數[執行階段](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)您應用程式組態檔區段：<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.UseInsecureHashAlgorithms=false;Switch.System.Security.Cryptography.Pkcs.UseInsecureHashAlgorithms=false&quot; /&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Security.Cryptography.Pkcs.CmsSigner?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.Reference?displayProperty=nameWithType></li></ul>|

