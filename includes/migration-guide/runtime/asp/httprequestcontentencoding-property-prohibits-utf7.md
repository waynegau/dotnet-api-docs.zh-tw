### <a name="httprequestcontentencoding-property-prohibits-utf7"></a>HttpRequest.ContentEncoding 屬性禁止 UTF7

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.5 開始，utf-7 編碼方式的禁止<xref:System.Web.HttpRequest?displayProperty=name>s' 內文。 在某些情況下，倚賴傳入 UTF-7 資料的應用程式資料將無法正確解碼。|
|建議|在理想情況下，應用程式應該更新為使用 utf-7 編碼方式<xref:System.Web.HttpRequest?displayProperty=name>s。 或者，您也可以使用 [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx) 項目的 <code>aspnet:AllowUtf7RequestContentEncoding</code> 屬性還原舊版行為。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|

