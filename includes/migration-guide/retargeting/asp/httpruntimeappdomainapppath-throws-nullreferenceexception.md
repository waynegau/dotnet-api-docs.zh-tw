### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath 擲回 NullReferenceException

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.6.2 中，執行階段會擲回<code>T:System.NullReferenceException</code>擷取時<code>P:System.Web.HttpRuntime.AppDomainAppPath</code>包含 null 字元的值。在.NET Framework 4.6.1 和更早版本中，執行階段會擲回<code>T:System.ArgumentNullException</code>。|
|建議|您可以執行其中一個後續回應給這項變更：<ul><li>處理<code>T:System.NullReferenceException</code>如果您的應用程式在.NET Framework 4.6.2 上執行。</li><li>升級至.NET Framework 4.7，還原先前的行為，並擲回<code>T:System.ArgumentNullException</code>。</li></ul>|
|範圍|Edge|
|版本|4.6.2|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

