### <a name="path-colon-checks-are-stricter"></a>路徑冒號檢查都是更嚴格

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.6.2 中，進行一些變更支援先前不支援的路徑 （無論長度和格式）。 如需適當的磁碟機的分隔符號 （冒號） 語法進行檢查更為正確，其中具有副作用的封鎖某些 URI 中的路徑中使用這些可容許的幾個選取的路徑 Api。|
|建議|如果您可以傳遞 URI 給受影響的應用程式開發介面，修改字串第一次是合法的路徑。<ul><li>以手動方式從 Url 移除配置 (例如移除<code>file://</code>從 Url)</li><li>傳遞至 URI<xref:System.Uri>類別，並且使用 <xref:System.Uri.LocalPath></li></ul>或者，您可以選擇不在新的路徑正規化藉由設定<code>Switch.System.IO.UseLegacyPathHandling</code>AppContext 參數為 true。|
|範圍|Edge|
|版本|4.6.2|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

