### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>WPF PackageDigitalSignatureManager 的預設雜湊演算法現在是 SHA256

|   |   |
|---|---|
|詳細資料|<code>System.IO.Packaging.PackageDigitalSignatureManager</code>提供的功能與 WPF 封裝的數位簽章。  在.NET Framework 4.7 和舊版中，預設的演算法 (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) 用來簽署封裝的組件是 SHA1。  因為新的安全性考量使用 SHA1，而這個預設值已變更為 SHA256 從.NET Framework 4.7.1 開始。  這項變更會影響所有封裝簽章，包括 XPS 文件。|
|建議|對於想要利用這項變更時以下方.NET 4.7.1 framework 版本為目標的開發人員或先前的功能需要同時以.NET 4.7.1 或更高的可為目標的開發人員請適當地設定下列 AppContext 旗標。  如果為 true 會導致 SHA1 做的預設演算法。SHA256 false 的結果。<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.7.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

