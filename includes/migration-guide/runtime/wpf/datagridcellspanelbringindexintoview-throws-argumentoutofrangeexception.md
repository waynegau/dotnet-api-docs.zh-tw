### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView 擲回 ArgumentOutOfRangeException

|   |   |
|---|---|
|詳細資料|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> 將以非同步方式運作時啟用資料行的虛擬化，但資料行寬度尚未決定。  如果資料行移除前非同步工作，<xref:System.ArgumentOutOfRangeException?displayProperty=name>可能會發生。|
|建議|下列任何一個：<ol><li>升級至.NET 4.7。</li><li>.Net 4.6.2 安裝最新的服務修補程式。</li><li>避免移除資料行，直到非同步回應<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)>已完成。</li></ol>|
|範圍|Edge|
|版本|4.6.2|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

