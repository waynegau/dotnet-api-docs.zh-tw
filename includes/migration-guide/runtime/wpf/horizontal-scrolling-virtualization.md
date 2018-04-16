### <a name="horizontal-scrolling-and-virtualization"></a><span data-ttu-id="90798-101">水平捲軸和虛擬化</span><span class="sxs-lookup"><span data-stu-id="90798-101">Horizontal scrolling and virtualization</span></span>

|   |   |
|---|---|
|<span data-ttu-id="90798-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="90798-102">Details</span></span>|<span data-ttu-id="90798-103">此變更套用到<xref:System.Windows.Controls.ItemsControl?displayProperty=name>會自己相交主要捲動的方向的方向中的虛擬化 (主要範例是<xref:System.Windows.Controls.DataGrid?displayProperty=name>EnableColumnVirtualization =&quot;True&quot;)。</span><span class="sxs-lookup"><span data-stu-id="90798-103">This change applies to an <xref:System.Windows.Controls.ItemsControl?displayProperty=name> that does its own virtualization in the direction orthogonal to the main scrolling direction (the chief example is <xref:System.Windows.Controls.DataGrid?displayProperty=name> with EnableColumnVirtualization=&quot;True&quot;).</span></span>  <span data-ttu-id="90798-104">特定的水平捲動作業的結果已變更，以產生結果更具直覺性且更類似於可比較的垂直作業的結果。作業包括&quot;這裡捲動&quot;和&quot;右邊緣&quot;，可使用從功能表取得，以滑鼠右鍵按一下水平捲軸的名稱。</span><span class="sxs-lookup"><span data-stu-id="90798-104">The outcome of certain horizontal scrolling operations has been changed to produce results that are more intuitive and more analogous to the results of comparable vertical operations.The operations include &quot;Scroll Here&quot; and &quot;Right Edge&quot;, to use the names from the menu obtained by right-clicking a horizontal scrollbar.</span></span>  <span data-ttu-id="90798-105">這兩種計算候選位移並呼叫<xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>。捲動至新的位移的概念後&quot;這裡&quot;或&quot;邊緣&quot;可能因為新取消虛擬化的內容已變更的值已變更<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>。 .Net 4.6.2 之前, 捲軸作業會直接使用的候選項目位移，即使它可能不是&quot;這裡&quot;或&quot;邊緣&quot;了。</span><span class="sxs-lookup"><span data-stu-id="90798-105">Both of these compute a candidate offset and call <xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>.After scrolling to the new offset, the notion of &quot;here&quot; or &quot;right edge&quot; may have changed because newly de-virtualized content has changed the value of <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>.Prior to .Net 4.6.2, the scroll operation simply uses the candidate offset, even though it may not be &quot;here&quot; or at the &quot;right edge&quot; any more.</span></span>  <span data-ttu-id="90798-106">這會導致等效果&quot;彈跳&quot;捲動縮圖，最佳範例所示。</span><span class="sxs-lookup"><span data-stu-id="90798-106">This results in effects like &quot;bouncing&quot; the scroll thumb, best illustrated by example.</span></span> <span data-ttu-id="90798-107">假設<xref:System.Windows.Controls.DataGrid?displayProperty=name>具有 ExtentWidth = 1000年和寬度 = 200。</span><span class="sxs-lookup"><span data-stu-id="90798-107">Suppose a <xref:System.Windows.Controls.DataGrid?displayProperty=name> has ExtentWidth=1000 and Width=200.</span></span>  <span data-ttu-id="90798-108">捲動至&quot;右邊緣&quot;使用候選位移 1000年-200 = 800。</span><span class="sxs-lookup"><span data-stu-id="90798-108">A scroll to &quot;Right Edge&quot; uses candidate offset 1000 - 200 = 800.</span></span>  <span data-ttu-id="90798-109">捲動到該位移，新的資料行是 de-虛擬化。讓我們假設它們是非常廣泛，以便<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>變更為 2000年。</span><span class="sxs-lookup"><span data-stu-id="90798-109">While scrolling to that offset, new columns are de- virtualized; let's suppose they are very wide, so that the <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name> changes to 2000.</span></span>  <span data-ttu-id="90798-110">捲軸的結尾是 HorizontalOffset = 800，且 thumb&quot;退&quot;回到捲軸的中央附近精確 800/2000年 = 40%處。當這種情況發生，並再試一次重新計算新的候選項目位移會變更。</span><span class="sxs-lookup"><span data-stu-id="90798-110">The scroll ends with HorizontalOffset=800, and the thumb &quot;bounces&quot; back to near the middle of the scrollbar - precisely at 800/2000 = 40%.The change is to recompute a new candidate offset when this situation occurs, and try again.</span></span> <span data-ttu-id="90798-111">(這是如何垂直捲動已經運作。)變更後產生的使用者，更可預測且直覺式的體驗，但它也可能會影響任何應用程式的確切值而定，<xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name>水平捲軸，是否叫用使用者或明確呼叫之後<xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>。</span><span class="sxs-lookup"><span data-stu-id="90798-111">(This is how vertical scrolling works already.)The change produces a more predictable and intuitive experience for the end user, but it could also affect any app that depends on the exact value of <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name> after a horizontal scroll, whether invoked by the end user or by an explicit call to <xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>.</span></span>|
|<span data-ttu-id="90798-112">建議</span><span class="sxs-lookup"><span data-stu-id="90798-112">Suggestion</span></span>|<span data-ttu-id="90798-113">使用的預測的值的應用程式<xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name>應該變更，以擷取實際的值 (和值<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>) 之後無法變更任何水平捲軸<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>因為取消的虛擬化。</span><span class="sxs-lookup"><span data-stu-id="90798-113">An app that uses a predicted value for <xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name> should be changed to fetch the actual value (and the value of <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>) after any horizontal scroll that could change <xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name> due to de-virtualization.</span></span>|
|<span data-ttu-id="90798-114">範圍</span><span class="sxs-lookup"><span data-stu-id="90798-114">Scope</span></span>|<span data-ttu-id="90798-115">次要</span><span class="sxs-lookup"><span data-stu-id="90798-115">Minor</span></span>|
|<span data-ttu-id="90798-116">版本</span><span class="sxs-lookup"><span data-stu-id="90798-116">Version</span></span>|<span data-ttu-id="90798-117">4.6.2</span><span class="sxs-lookup"><span data-stu-id="90798-117">4.6.2</span></span>|
|<span data-ttu-id="90798-118">類型</span><span class="sxs-lookup"><span data-stu-id="90798-118">Type</span></span>|<span data-ttu-id="90798-119">執行階段</span><span class="sxs-lookup"><span data-stu-id="90798-119">Runtime</span></span>|
|<span data-ttu-id="90798-120">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="90798-120">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.Primitives.IScrollInfo?displayProperty=nameWithType></li></ul>|
