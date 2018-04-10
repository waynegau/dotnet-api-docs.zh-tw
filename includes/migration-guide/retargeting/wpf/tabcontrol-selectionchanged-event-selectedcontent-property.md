### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>TabControl SelectionChanged 事件和 SelectedContent 屬性

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.7.1，開始<xref:System.Windows.Controls.TabControl>值更新其<xref:System.Windows.Controls.TabControl.SelectedContent>屬性引發之前<xref:System.Windows.Controls.Primitives.Selector.SelectionChanged>當其選取項目變更時引發的事件。在.NET Framework 4.7 和更早版本中，更新 SelectedContent 發生事件之後。|
|建議|目標為.NET Framework 4.7.1 或更新版本可以退出此應用程式變更，並使用舊版行為新增至以下<code>&lt;runtime&gt;</code>應用程式組態檔區段：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>目標為.NET Framework 4.7 或舊版，但應用程式在.NET Framework 4.7.1 上正在執行，或稍後可以啟用新的行為將下列這一行加入<code>&lt;runtime&gt;</code>應用程式.configuration 檔區段：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

