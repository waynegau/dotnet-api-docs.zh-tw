### <a name="etw-eventlisteners-do-not-capture-events-from-providers-with-explicit-keywords-like-the-tpl-provider"></a>ETW EventListeners 不會擷取與明確的關鍵字 （例如 TPL 提供者） 提供者事件

|   |   |
|---|---|
|詳細資料|具有空白關鍵字遮罩的 ETW EventListeners 無法使用 Explicit 關鍵字從提供者正確地擷取事件。 在 .NET Framework 4.5 中，TPL 提供者已開始提供 Explicit 關鍵字並觸發此問題。 在 .NET Framework 4.6 中，已更新 EventListeners，因此不會再發生此問題。|
|建議|若要解決這個問題，取代呼叫<xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)>明確指定 EnableEvents 多載呼叫&quot;任何關鍵字&quot;遮罩，以使用： <code>EnableEvents(eventSource, level, unchecked((EventKeywords)0xFFFFffffFFFFffff))</code>。或者，此問題在.NET Framework 4.6 中已修正問題，而且定址方式可透過升級至.NET Framework 的版本。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Diagnostics.Tracing.EventListener.EnableEvents(System.Diagnostics.Tracing.EventSource,System.Diagnostics.Tracing.EventLevel)?displayProperty=nameWithType></li></ul>|

