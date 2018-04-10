### <a name="resizing-a-grid-can-hang"></a>調整大小的方格會當機

|   |   |
|---|---|
|詳細資料|配置期間可能發生無限迴圈<code>T:System.Windows.Controls.Grid</code>在下列情況：<ul><li>資料列定義包含兩個 *-資料列，這兩個宣告，MinHeight 和 MaxHeight。</li><li>內容的 *-資料列不會超過對應 MaxHeight</li><li>方格的可用高度超過第一個 MinHeight （加上任何其他固定或自動的資料列）</li><li>應用程式為目標.Net 4.7，或選擇加入 4.7 配置演算法藉由設定 <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>與兩個以上的資料列，或類似案例中的資料行，也會發生迴圈。在.Net 4.7.1 修正問題。|
|建議|升級至.Net 4.7.1。  或者，如果您不需要 4.7 配置演算法，您可以使用下列組態設定：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.7|
|類型|執行階段|

