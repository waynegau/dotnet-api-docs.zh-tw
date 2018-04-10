### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>捲動 WPF 樹狀檢視或群組的清單方塊中 VirtualizingStackPanel 可能會造成停止回應

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.5 版中，捲動 WPF<xref:System.Windows.Controls.TreeView?displayProperty=name>在虛擬化堆疊面板可能會導致擱置如果在檢視區邊界 (中的項目之間<xref:System.Windows.Controls.TreeView?displayProperty=name>，比方說，或 ItemsPresenter 項目上)。 此外，在某些情況下，即使沒有邊界，檢視中不同大小的項目也可能會造成不穩定的情況。|
|建議|您可以升級至 .NET Framework 4.5.1 來避免此錯誤 (bug)。 或者，可以從檢視集合移除邊界 (例如<xref:System.Windows.Controls.TreeView?displayProperty=name>s) 中虛擬化堆疊面板，如果所有包含的項目大小都一樣。|
|範圍|主要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

