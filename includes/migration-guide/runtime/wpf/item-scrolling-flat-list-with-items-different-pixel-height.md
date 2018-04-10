### <a name="item-scrolling-a-flat-list-with-items-of-different-pixel-height"></a>項目捲動一般具有不同像素高度的項目清單

|   |   |
|---|---|
|詳細資料|當<xref:System.Windows.Controls.ItemsControl?displayProperty=name>顯示使用虛擬化的集合 (<code>IsVirtualizing=true</code>) 和項目-捲動 (<code>ScrollUnit=Item</code>)，以及當控制項捲動至顯示的項目與相鄰項目，其高度，單位為像素為單位<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>逐一查看所有集合中的項目。 在這個反覆項目; UI 沒有回應如果集合很大，這可以視為無回應。在反覆項目就會發生在其他情況下，即使是在之前的.Net 版本。 比方說，它發生於捲動的像素 (<code>ScrollUnit=Pixel</code>) 項目捲動時，遇到項目具有不同像素高度及時階層式資料 (例如<xref:System.Windows.Controls.TreeView?displayProperty=name>或<xref:System.Windows.Controls.ItemsControl?displayProperty=name>與啟用的群組) 時遇到的項目。不同的子系的項目與相鄰項目數目。項目捲動和不同的像素高度案例中，若要修正 bug 的階層式資料版面配置中的.Net 4.6.1 中引進了反覆項目。  不需要如果是一般 （沒有階層），且.Net 4.6.2 就不會執行在此情況下的資料。|
|建議|如果反覆項目，就會發生在.Net 4.6.1 但不是在較早的版本-也就是如果<xref:System.Windows.Controls.ItemsControl?displayProperty=name>是項目-捲動一般清單使用的不同像素高度的項目中，有兩種解決方法：<ol><li>安裝.Net 4.6.2。</li><li>安裝 hotfix HR 1605.net 4.6.1。</li></ol>|
|範圍|次要|
|版本|4.6.1|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=nameWithType></li></ul>|

