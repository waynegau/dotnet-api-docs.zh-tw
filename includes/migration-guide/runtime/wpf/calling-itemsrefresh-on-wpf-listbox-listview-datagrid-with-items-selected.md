### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>WPF 清單方塊、 清單檢視或資料格中選取的項目上呼叫 Items.Refresh 可能會導致重複的項目會出現在項目

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.5 中選取項目時，從程式碼呼叫 ListBox.Items.Refresh<xref:System.Windows.Controls.ListBox?displayProperty=name>可能會導致複製清單中選取的項目。 類似的問題，就會發生與<xref:System.Windows.Controls.ListView?displayProperty=name>和<xref:System.Windows.Controls.DataGrid?displayProperty=name>。 這在 .NET Framework 4.6 中已修正。|
|建議|可能會解決這個問題以程式設計方式控制程式取消選取項目之前<xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name>稱為，然後在呼叫完成之後重新選取。 此外，此問題在 .NET Framework 4.6 中已修正，因此可藉由升級至該版 .NET Framework 來解決。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

