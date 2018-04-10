### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>從 SelectedItems Items.Clear 不會移除重複項目

|   |   |
|---|---|
|詳細資料|選取器 （啟用多個選取項目） 有重複項目假設其<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>集合-相同的項目出現一次以上。  從資料來源中移除這些項目 （例如藉由呼叫 Items.Clear） 就無法移除從<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>; 只會移除第一個執行個體。 此外，後續使用<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>(例如 SelectedItems.Clear()) 可能會發生問題例如<xref:System.ArgumentException?displayProperty=name>，因為<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>包含已經不在資料來源中的項目。|
|建議|.NET 4.6.2 盡可能升級。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

