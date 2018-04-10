### <a name="glyphruncomputeinkboundingbox-and-formattedtextextent-return-different-values-beginning-in-net-45"></a>GlyphRun.ComputeInkBoundingBox() 和 FormattedText.Extent 傳回不同的值從.NET 4.5 開始

|   |   |
|---|---|
|詳細資料|已改進<xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox>和<xref:System.Windows.Media.FormattedText.Extent>在.NET Framework 4.5，來解決問題，其中的方塊已在某些情況下，.NET Framework 4.0 中包含的圖像太小。 因此，從 .NET Framework 4.5 開始，某些週框方塊會比較大，導致 UI 配置中有些微差異。|
|建議|請注意，某些字符週框方塊大小已增加。 這些變更通常會改進呈現方式和叫用方塊測試，但如果想要舊版 (.NET 4.5 之前) 行為，則可以將下列項目新增至 app.config 檔案來加入此行為：<pre><code class="language-xml">&lt;appsettings&gt;&#13;&#10;&lt;add key=&quot;IncludeAllInkInBoundingBox&quot; value=&quot;false&quot;&gt;&#13;&#10;&lt;/appsettings&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox?displayProperty=nameWithType></li><li><xref:System.Windows.Media.FormattedText.Extent?displayProperty=nameWithType></li></ul>|

