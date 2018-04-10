### <a name="xslt-forward-compat-now-works"></a>XSLT 正向相容現在的運作方式

|   |   |
|---|---|
|詳細資料|在.NET Framework 4 中，XSLT 1.0 往後相容性有下列問題：<ul><li>如果樣式表的版本設為 2.0，而且剖析器遇到無法辨識的 XSLT 1.0 結構，則載入樣式表會失敗。</li><li>如果樣式表版本設為 1.1，<code>xsl:sort</code> 結構就無法排序資料。</li></ul>.NET Framework 4.5、 這些問題已獲得修正，而且 XSLT 1.0 往後相容性模式可正常運作。|
|建議|大部分的應用程式應該不會受到影響，不過資料的排序方式在某些情況下，現在 sort 遵守。 如果<code>xsl:sort</code>是使用 1.1 版的樣式表中，確認應用程式不根據資料的排序次序。 如果應用程式依賴排序行為 4.0，請移除<code>xsl:sort</code>從樣式表。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

