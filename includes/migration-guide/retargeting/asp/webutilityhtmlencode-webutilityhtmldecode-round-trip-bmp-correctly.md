### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode 和 WebUtility.HtmlDecode 反覆存取 BMP 正確

|   |   |
|---|---|
|詳細資料|目標.NET Framework 4.5、 字元以外的基本多語文平面 (BMP) 來回正確時傳遞至的應用程式<xref:System.Net.WebUtility.HtmlDecode(System.String)>方法。|
|建議|這項變更應該不會影響目前的應用程式，但若要還原原始行為，設定<code>targetFramework</code>屬性<code>&lt;httpRuntime&gt;</code>字串以外的項目&quot;4.5&quot;。 您也可以設定 <code>unicodeEncodingConformance</code> 組態項目的 <code>unicodeDecodingConformance</code> 和 <code>&lt;webUtility&gt;</code> 屬性，以與目標 .NET Framework 版本不相關的方式控制這個行為。|
|範圍|Edge|
|版本|4.5|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

