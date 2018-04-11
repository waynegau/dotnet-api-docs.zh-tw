### <a name="horizontal-scrolling-and-virtualization"></a>水平捲軸和虛擬化

|   |   |
|---|---|
|詳細資料|此變更套用到<xref:System.Windows.Controls.ItemsControl?displayProperty=name>會自己相交主要捲動的方向的方向中的虛擬化 (主要範例是<xref:System.Windows.Controls.DataGrid?displayProperty=name>EnableColumnVirtualization =&quot;True&quot;)。  特定的水平捲動作業的結果已變更，以產生結果更具直覺性且更類似於可比較的垂直作業的結果。作業包括&quot;這裡捲動&quot;和&quot;右邊緣&quot;，可使用從功能表取得，以滑鼠右鍵按一下水平捲軸的名稱。  這兩種計算候選位移並呼叫<xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>。捲動至新的位移的概念後&quot;這裡&quot;或&quot;邊緣&quot;可能因為新取消虛擬化的內容已變更的值已變更<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>。 .Net 4.6.2 之前, 捲軸作業會直接使用的候選項目位移，即使它可能不是&quot;這裡&quot;或&quot;邊緣&quot;了。  這會導致等效果&quot;彈跳&quot;捲動縮圖，最佳範例所示。 假設<xref:System.Windows.Controls.DataGrid?displayProperty=name>具有 ExtentWidth = 1000年和寬度 = 200。  捲動至&quot;右邊緣&quot;使用候選位移 1000年-200 = 800。  捲動到該位移，新的資料行是 de-虛擬化。讓我們假設它們是非常廣泛，以便<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>變更為 2000年。  捲軸的結尾是 HorizontalOffset = 800，且 thumb&quot;退&quot;回到捲軸的中央附近精確 800/2000年 = 40%處。當這種情況發生，並再試一次重新計算新的候選項目位移會變更。 (這是如何垂直捲動已經運作。)變更後產生的使用者，更可預測且直覺式的體驗，但它也可能會影響任何應用程式的確切值而定，<xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name>水平捲軸，是否叫用使用者或明確呼叫之後<xref:System.Windows.Controls.Primitives.IScrollInfo.SetHorizontalOffset(System.Double)>。|
|建議|使用的預測的值的應用程式<xref:System.Windows.Controls.Primitives.IScrollInfo.HorizontalOffset?displayProperty=name>應該變更，以擷取實際的值 (和值<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>) 之後無法變更任何水平捲軸<xref:System.Windows.Controls.Primitives.IScrollInfo.ExtentWidth?displayProperty=name>因為取消的虛擬化。|
|範圍|次要|
|版本|4.6.2|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Controls.Primitives.IScrollInfo?displayProperty=nameWithType></li></ul>|

