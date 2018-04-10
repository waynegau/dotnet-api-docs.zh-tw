### <a name="signedxml-and-encryptedxml-breaking-changes"></a>SignedXml 和 EncryptedXml 重大變更

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.6.2 安全性修正在<xref:System.Security.Cryptography.Xml.SignedXml?displayProperty=name>和<xref:System.Security.Cryptography.Xml.EncryptedXml?displayProperty=name>會導致不同的執行階段行為。 例如，套用至物件的<ul><li>如果文件有多個相同項目<code>id</code>屬性和簽章的目標其中一個這些項目為簽章的根，文件現在會視為無效。</li><li>使用非標準 XPath 轉換演算法在參考文件都視為無效。</li><li>使用非標準的 XSLT 轉換演算法在參考的文件會視為無效。</li><li>若要這樣做將無法使用卸離的外部資源的簽章中的任何程式並利用。</li></ul>|
|建議|開發人員可能會想要檢閱的用法<xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>和<xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform>，以及其他類型衍生自<xref:System.Security.Cryptography.Xml.Transform>因為文件接收者無法處理它。|
|範圍|次要|
|版本|4.6.2|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Security.Cryptography.Xml.Transform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXPathTransform?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.Xml.XmlDsigXsltTransform?displayProperty=nameWithType></li></ul>|

