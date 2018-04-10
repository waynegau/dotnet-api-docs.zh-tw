### <a name="the-replace-method-in-odata-urls-is-disabled-by-default"></a>預設為停用 OData Url 中的取代方法

|   |   |
|---|---|
|詳細資料|從 .NET Framework 4.5 開始，OData URL 中的 Replace 方法預設為停用。 當 OData Replace 停用 (現在為預設) 時，任何包含取代功能的使用者要求 (不常見) 將會失敗。|
|建議|如果需要 replace 方法 （此為罕見），就可以重新啟用透過組態設定 (<xref:System.Data.Services.Configuration.DataServicesFeaturesSection.ReplaceFunction?displayProperty=name>)。 不過，已啟用的 Replace 方法可能會有資訊安全漏洞，因此只有在仔細檢閱之後才能使用。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Data.Services.DataService%601?displayProperty=nameWithType></li></ul>|

