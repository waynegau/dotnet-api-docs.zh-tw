### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException 現在設定列位置正確

|   |   |
|---|---|
|詳細資料|如果<xref:System.Xml.Linq.LoadOptions.SetLineInfo>值會傳遞給 Load 方法且發生驗證錯誤，<xref:System.Xml.Schema.XmlSchemaException.LineNumber>和<xref:System.Xml.Schema.XmlSchemaException.LinePosition>屬性現在會包含行資訊。|
|建議|例外狀況處理程式碼假設<xref:System.Xml.Schema.XmlSchemaException.LineNumber>和<xref:System.Xml.Schema.XmlSchemaException.LinePosition>將不會因為這些屬性現在會設定正確載入 XML 時使用 SetLineInfo 時，就應該更新集。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

