### <a name="contentdisposition-datetimes-returns-slightly-different-string"></a>ContentDisposition Datetime 傳回稍有不同的字串

|   |   |
|---|---|
|詳細資料|字串表示的<xref:System.Net.Mime.ContentDisposition?displayProperty=name>的已更新，從 4.6，一律表示的小時元件<xref:System.DateTime?displayProperty=name>具有兩個位數。 這是為了遵守 [RFC822](http://www.ietf.org/rfc/rfc0822.txt) 和 [RFC2822](http://www.ietf.org/rfc/rfc2822.txt)。 這會導致 <xref:System.Net.Mime.ContentDisposition.ToString> 在 4.6 中傳回稍微不同的字串，例如，當其中一個配置的時間項目早於上午 10:00 時。 請注意，透過將它們轉換成字串，因此任何有時序列化 ContentDispositions<xref:System.Net.Mime.ContentDisposition.ToString>作業、 序列化或 GetHashCode 呼叫，則應檢閱。|
|建議|在不同的 .NET Framework 版本中，ContentDispositions 的字串表示不會正確地相互比較。 如果可能的話，請將字串轉換回 ContentDispositions，再進行比較。|
|範圍|次要|
|版本|4.6|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Net.Mime.ContentDisposition.ToString?displayProperty=nameWithType></li><li><xref:System.Net.Mime.ContentDisposition.GetHashCode?displayProperty=nameWithType></li></ul>|

