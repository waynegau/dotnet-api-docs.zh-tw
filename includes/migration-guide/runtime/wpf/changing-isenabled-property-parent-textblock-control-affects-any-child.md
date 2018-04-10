### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>IsEnabled 屬性 TextBlock 控制項的父代的變更會影響任何子控制項

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.6.2，變更<xref:System.Windows.UIElement.IsEnabled?displayProperty=name>屬性的父代<xref:System.Windows.Controls.TextBlock?displayProperty=name>控制影響 （例如超連結和按鈕） 的任何子控制項<xref:System.Windows.Controls.TextBlock?displayProperty=name>控制項。在.NET Framework 4.6.1 和更早版本中，控制內<xref:System.Windows.Controls.TextBlock?displayProperty=name>不一定反映狀態<xref:System.Windows.UIElement.IsEnabled?displayProperty=name>屬性<xref:System.Windows.Controls.TextBlock?displayProperty=name>父代。|
|建議|無。 這項變更符合 <xref:System.Windows.Controls.TextBlock?displayProperty=name> 控制項內的之控制項的預期行為。|
|範圍|次要|
|版本|4.6.2|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|

