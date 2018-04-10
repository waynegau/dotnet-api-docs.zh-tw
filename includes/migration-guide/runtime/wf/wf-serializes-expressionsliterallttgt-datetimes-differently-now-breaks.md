### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF 序列化 Expressions.Literal&lt;T&gt; Datetime 以不同方式現在 （中斷自訂 XAML 剖析器）

|   |   |
|---|---|
|詳細資料|相關聯<xref:System.Windows.Markup.ValueSerializer>物件會將轉換<xref:System.DateTime?displayProperty=name>或<xref:System.DateTimeOffset?displayProperty=name>第二個物件，其與<xref:System.DateTime.Millisecond?displayProperty=name>元件為非零和 (如<xref:System.DateTime?displayProperty=name>值) 其<xref:System.DateTime.Kind>屬性不是屬性項目未指定而非字串的語法。 這項變更會允許往返 <xref:System.DateTime?displayProperty=name> 和 <xref:System.DateTimeOffset?displayProperty=name> 值。 假設輸入 XAML 是使用屬性語法的自訂 XAML 剖析器將無法正常運作。|
|建議|這項變更會允許往返 <xref:System.DateTime?displayProperty=name> 和 <xref:System.DateTimeOffset?displayProperty=name> 值。 假設輸入 XAML 是使用屬性語法的自訂 XAML 剖析器將無法正常運作。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|

