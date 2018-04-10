### <a name="wpf-treeviewitem-must-be-used-within-a-treeview"></a>必須樹狀檢視中使用 WPF TreeViewItem

|   |   |
|---|---|
|詳細資料|限制的使用量 4.5 中的變更所導入<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>以外的項目<xref:System.Windows.Controls.TreeView?displayProperty=name>。 在下列狀況下可能會發生這種情形：<ul><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name>視覺化父項目不是 panel。 (A<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>產生<xref:System.Windows.Controls.TreeView?displayProperty=name>必須為其父系的面板)</li><li><xref:System.Windows.Controls.TreeViewItem?displayProperty=name>是的下階<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>做為&quot;項目主機&quot;清單控制項 （清單方塊中，資料格、 ListView 等等）。 不需要啟用虛擬化。</li><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>是項目捲動 (<code>ScrollUnit=&quot;Item&quot;</code>)。</li><li>使用者可呼叫 <code>VirtualizingStackPanel.MakeVisible(v)</code> 將項目 <code>v</code> 捲動至檢視中。 這可以透過數種方式明確或隱含完成；最常見的方式可能是直接按一下 <code>v</code> 以提供鍵盤焦點。</li><li>從視覺父鏈結<code>v</code>至<xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name>通過<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>。</li></ul>換句話說，此情況時<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>使用外部<xref:System.Windows.Controls.TreeView?displayProperty=name>，且使用者按一下的下階<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>將帶入檢視。 如果<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>沒有可設定焦點的下階，您永遠不會看到這個問題。 遇到這種情況的範例是當<xref:System.Windows.Controls.TreeViewItem?displayProperty=name>是 DataTemplate 的根。 遇到此問題時，WPF 架構內會出現 InvalidCastException。|
|建議|未來將針對此問題提供 Hotfix。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|

