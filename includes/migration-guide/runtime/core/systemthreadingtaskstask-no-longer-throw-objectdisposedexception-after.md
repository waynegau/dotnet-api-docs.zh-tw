### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>System.Threading.Tasks.Task 不再之後會擲回 ObjectDisposedException 處置物件

|   |   |
|---|---|
|詳細資料|除了<xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>，<xref:System.Threading.Tasks.Task?displayProperty=name>方法不會再擲回<xref:System.ObjectDisposedException?displayProperty=name>處置物件後的例外狀況。這項變更支援使用快取的工作。 例如，方法可能傳回快取的工作來表示已完成的作業，而不配置新的工作。 舊版的 .NET Framework 並未提供這項功能，因為工作的任何消費者都可能會處置它，使它變得無法使用。|
|建議|請注意工作方法可能不會擲回<xref:System.ObjectDisposedException?displayProperty=name>情況下在處置物件。 如果應用程式已根據知道工作已處置此例外狀況，應該更新明確檢查工作的狀態使用<xref:System.Threading.Tasks.Task.Status>。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|

