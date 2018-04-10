### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>System.Uri.IsWellFormedUriString 方法的第一個區段中的冒號字元與相對 Uri 會傳回 false

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.5、<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)>會將與相對 Uri<code>:</code>不正確，因為其第一個區段中。 這是來自變更<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name>以符合對 RFC3986.NET Framework 4.0 中的行為。|
|建議|這項變更 （例如，許多其他的 URI 變更） 只會影響應用程式的.NET framework 4.5 （或更新版本）。 若要繼續使用舊的行為，目標應用程式針對.NET Framework 4.0。 或者，在呼叫前掃描 URI 的<xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name>尋找<code>:</code>如果舊的行為，您可能想要進行驗證時，移除的字元。|
|範圍|次要|
|版本|4.5|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

