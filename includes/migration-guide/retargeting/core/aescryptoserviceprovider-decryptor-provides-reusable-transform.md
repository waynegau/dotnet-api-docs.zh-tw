### <a name="aescryptoserviceprovider-decryptor-provides-a-reusable-transform"></a>AesCryptoServiceProvider 的解密程式來提供可重複使用的轉換

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.6.2，為目標的應用程式開始<xref:System.Security.Cryptography.AesCryptoServiceProvider>的解密程式來提供可重複使用的轉換。 呼叫 <xref:System.Security.Cryptography.CryptoAPITransform.TransformFinalBlock(System.Byte[],System.Int32,System.Int32)?displayProperty=name> 之後，轉換就會重新初始化並且可重複使用。 針對以舊版.NET Framework 為目標的應用程式，嘗試將重複的解密程式來使用藉由呼叫<xref:System.Security.Cryptography.CryptoAPITransform.TransformBlock(System.Byte[],System.Int32,System.Int32,System.Byte[],System.Int32)?displayProperty=name>呼叫之後<xref:System.Security.Cryptography.CryptoAPITransform.TransformFinalBlock(System.Byte[],System.Int32,System.Int32)?displayProperty=name>會擲回<xref:System.Security.Cryptography.CryptographicException>或產生的資料損毀。|
|建議|由於這是預期的行為，此變更影響應該很小。相依於先前的行為的應用程式可以選擇不使用加上下列組態設定加入<code>&lt;runtime&gt;</code>應用程式的組態檔區段：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.AesCryptoServiceProvider.DontCorrectlyResetDecryptor=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>此外，舊版.NET Framework 為目標，但在以.NET Framework 4.6.2 啟動.NET Framework 版本下執行的應用程式也可以選擇它藉由將下列組態設定來<code>&lt;runtime&gt;</code>區段應用程式的組態檔：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.AesCryptoServiceProvider.DontCorrectlyResetDecryptor=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.6.2|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Security.Cryptography.AesCryptoServiceProvider.CreateDecryptor?displayProperty=nameWithType></li></ul>|

