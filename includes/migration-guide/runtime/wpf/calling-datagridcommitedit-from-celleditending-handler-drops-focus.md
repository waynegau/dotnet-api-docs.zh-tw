### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a><span data-ttu-id="27b9b-101">從 CellEditEnding 處理常式呼叫 DataGrid.CommitEdit 卸除焦點</span><span class="sxs-lookup"><span data-stu-id="27b9b-101">Calling DataGrid.CommitEdit from a CellEditEnding handler drops focus</span></span>

|   |   |
|---|---|
|<span data-ttu-id="27b9b-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="27b9b-102">Details</span></span>|<span data-ttu-id="27b9b-103">呼叫<xref:System.Windows.Controls.DataGrid.CommitEdit>從其中一個<xref:System.Windows.Controls.DataGrid?displayProperty=name>的<xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name>事件處理常式會導致<xref:System.Windows.Controls.DataGrid?displayProperty=name>失去焦點。</span><span class="sxs-lookup"><span data-stu-id="27b9b-103">Calling <xref:System.Windows.Controls.DataGrid.CommitEdit> from one of the <xref:System.Windows.Controls.DataGrid?displayProperty=name>'s <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> event handlers causes the <xref:System.Windows.Controls.DataGrid?displayProperty=name> to lose focus.</span></span>|
|<span data-ttu-id="27b9b-104">建議</span><span class="sxs-lookup"><span data-stu-id="27b9b-104">Suggestion</span></span>|<span data-ttu-id="27b9b-105">此錯誤 (bug) 在 .NET Framework 4.5.2 中已修正，因此可藉由升級 .NET Framework 來避免。</span><span class="sxs-lookup"><span data-stu-id="27b9b-105">This bug has been fixed in the .NET Framework 4.5.2, so it can be avoided by upgrading the .NET Framework.</span></span> <span data-ttu-id="27b9b-106">或者，明確地重新選取避免<xref:System.Windows.Controls.DataGrid?displayProperty=name>之後呼叫<xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>。</span><span class="sxs-lookup"><span data-stu-id="27b9b-106">Alternatively, it can be avoided by explicitly re-selecting the <xref:System.Windows.Controls.DataGrid?displayProperty=name> after calling <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.</span></span>|
|<span data-ttu-id="27b9b-107">範圍</span><span class="sxs-lookup"><span data-stu-id="27b9b-107">Scope</span></span>|<span data-ttu-id="27b9b-108">Edge</span><span class="sxs-lookup"><span data-stu-id="27b9b-108">Edge</span></span>|
|<span data-ttu-id="27b9b-109">版本</span><span class="sxs-lookup"><span data-stu-id="27b9b-109">Version</span></span>|<span data-ttu-id="27b9b-110">4.5</span><span class="sxs-lookup"><span data-stu-id="27b9b-110">4.5</span></span>|
|<span data-ttu-id="27b9b-111">類型</span><span class="sxs-lookup"><span data-stu-id="27b9b-111">Type</span></span>|<span data-ttu-id="27b9b-112">執行階段</span><span class="sxs-lookup"><span data-stu-id="27b9b-112">Runtime</span></span>|
|<span data-ttu-id="27b9b-113">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="27b9b-113">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|
