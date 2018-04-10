### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>GridViews AllowCustomPaging 設定設為 true 可能 PageIndexChanging 時引發事件保留在檢視中的最後一頁

|   |   |
|---|---|
|詳細資料|.NET Framework 4.5 中的 bug 會導致<xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name>有時不會針對引發<xref:System.Web.UI.WebControls.GridView?displayProperty=name>已啟用的 s <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>。|
|建議|.NET Framework 4.6 中已修正此問題，而且定址方式可透過升級至.NET Framework 的版本。 為解決方法是，應用程式可執行任何明確 BindGrid <code>Page_Load</code> ，會叫用這些條件 (<xref:System.Web.UI.WebControls.GridView?displayProperty=name>是最後一個頁面及最後一個<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>不同<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>)。 或者，應用程式會修改成允許分頁 （而不是自訂分頁） 上，如這種情況下不會示範此問題。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

