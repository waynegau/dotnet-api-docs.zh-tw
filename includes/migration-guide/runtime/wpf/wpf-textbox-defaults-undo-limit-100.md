### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>WPF 文字方塊中，則預設為復原限制為 100

|   |   |
|---|---|
|詳細資料|在 .NET 4.5 中，WPF TextBox 的預設復原限制為 100 (在 .NET 4.0 中則沒有限制)|
|建議|如果復原限制為 100 太低，限制可以明確設定與 <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

