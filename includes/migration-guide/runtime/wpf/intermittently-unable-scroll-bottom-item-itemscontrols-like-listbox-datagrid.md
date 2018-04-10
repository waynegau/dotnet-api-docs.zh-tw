### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>間歇地無法捲動至底部 ItemsControls （例如清單方塊和資料格） 中的項目使用自訂 DataTemplates 時

|   |   |
|---|---|
|詳細資料|在某些情況下，.NET Framework 4.5 中的錯誤造成 ItemsControls (像是<xref:System.Windows.Controls.ListBox?displayProperty=name>， <xref:System.Windows.Controls.ComboBox?displayProperty=name>，<xref:System.Windows.Controls.DataGrid?displayProperty=name>等等) 要使用自訂 DataTemplates 時捲動至其下方項目。 如果嘗試捲動第二次 (在向上捲動之後)，則會再次運作。|
|建議|此問題在 .NET Framework 4.5.2 中已修正，因此可藉由升級至該版 .NET Framework (或更新版本) 來解決。 此外，使用者仍可將捲軸拖曳至這些集合中的最後一個項目，但可能需要嘗試兩次才能成功。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|

