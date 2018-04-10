### <a name="dataobjectgetdata-now-retrieves-data-as-utf-8"></a>為 utf-8 DataObject.GetData 立即擷取的資料

|   |   |
|---|---|
|詳細資料|應用程式的目標.NET Framework 4 或.NET Framework 4.5.1 或舊版中，執行<code>DataObject.GetData</code>擷取 HTML 格式的資料為 ASCII 字串。 如此一來，非 ASCII 字元 （字元的 ASCII 碼大於 0x7F） 是由兩個隨機字元表示。若是目標為.NET Framework 4.5 或更新版本及.NET Framework 4.5.2 上執行的應用程式<code>DataObject.GetData</code>擷取 HTML 格式的資料為 utf-8，其中可以正確地表示大於 0x7F 的字元。|
|建議|如果您實作 HTML 格式字串的編碼問題的因應措施 (例如，藉由明確地編碼的 HTML 字串擷取從剪貼簿傳遞至<xref:System.Text.UTF8Encoding.GetString(System.Byte[],System.Int32,System.Int32)?displayProperty=name>) 和重定應用程式版本為 4.5 版 4，因應措施就應該移除。如果因故需要舊的行為，應用程式可鎖定目標的.NET Framework 4.0，以取得該行為。|
|範圍|Edge|
|版本|4.5.2|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Windows.DataObject.GetData(System.String)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.Type)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

