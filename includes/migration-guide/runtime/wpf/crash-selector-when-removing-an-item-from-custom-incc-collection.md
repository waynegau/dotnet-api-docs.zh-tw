### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>當從自訂 INCC 集合中移除項目選取器中損毀

|   |   |
|---|---|
|詳細資料|<code>T:System.InvalidOperationException</code>可能會發生在下列案例：<ul><li>Datagridcellspresenter<code>T:System.Windows.Controls.Primitives.Selector</code>是集合的自訂實作與<code>T:System.Collections.Specialized.INotifyCollectionChanged</code>。</li><li>從集合中，移除選取的項目。</li><li><code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code>具有<code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code>=-1 （表示未知的位置）。</li></ul>例外狀況的呼叫堆疊的開頭位於 System.Windows.Threading.Dispatcher.VerifyAccess() 在 System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject System.Windows.DependencyObject.GetValue (DependencyProperty dp)項目） 在.Net 4.5 中可以發生此例外狀況，如果應用程式都有一個以上的發送器執行緒。 在.Net 4.7 也可以與單一發送器執行緒的應用程式中發生例外狀況。 在.Net 4.7.1 修正問題。|
|建議|升級至.Net 4.7.1。|
|範圍|次要|
|版本|4.7|
|類型|執行階段|

