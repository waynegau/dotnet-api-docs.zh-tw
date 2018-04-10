### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>從 DataGrid 的 UnloadingRow 事件處理常式存取 WPF DataGrid 的選取項目可能會導致 NullReferenceException

|   |   |
|---|---|
|詳細資料|由於.NET Framework 4.5 的事件處理常式中的 bug<xref:System.Windows.Controls.DataGrid>涉及一個資料列中的移除的事件可能會導致<xref:System.NullReferenceException?displayProperty=name>如它們存取擲回<xref:System.Windows.Controls.DataGrid>的<xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name>或<xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>屬性。|
|建議|.NET Framework 4.6 中已修正此問題，而且定址方式可透過升級至.NET Framework 的版本。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

