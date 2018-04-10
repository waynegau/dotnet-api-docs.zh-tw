### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>在具有逾時引數的 Task.WaitAll 方法的行為變更

|   |   |
|---|---|
|詳細資料|Task.WaitAll 行為中已提出更一致.NET 4.5.In.NET Framework 4 中，這些方法的行為不一致。 逾時過期時，如果在方法呼叫之前已完成或取消一個或多個工作，則方法會擲回 <xref:System.AggregateException?displayProperty=name> 例外狀況。 當逾時過期時，如果在方法呼叫之前沒有任何已完成或取消的工作，但是有一個或多個工作在方法呼叫之後進入這兩種狀態，則方法會傳回 false。<br/><br/>在.NET Framework 4.5、 這些方法多載現在會傳回 false 的任何工作仍在執行時的逾時間隔到期時，會擲回<xref:System.AggregateException?displayProperty=name>才在取消輸入的工作 （不論它是否在方法前後的例外狀況呼叫） 和任何其他工作仍在執行。|
|建議|如果<xref:System.AggregateException?displayProperty=name>已攔截到的偵測工作已取消之前所叫用的 WaitAll 呼叫程式碼應該改用方式透過 IsCanceled 屬性相同的偵測方法 (例如:。Any(t =&gt; t.IsCanceled)) 因為.NET 4.6 將只會擲回在此情況下若逾時之前完成所有等候的工作。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

