### <a name="xml-schema-validation-is-stricter"></a>XML 結構描述驗證更為嚴格

|   |   |
|---|---|
|詳細資料|.NET Framework 4.5、 XML 結構描述驗證是更嚴格。 如果您使用 xsd:anyURI 驗證 URI (例如 mailto 通訊協定)，而 URI 中有空格，則驗證會失敗。 在舊版 .NET Framework 中，驗證會成功。 變更會影響只有應用程式的.NET Framework 4.5 為目標。|
|建議|如果需要鬆散的.NET Framework 4.0 驗證，驗證的應用程式可鎖定目標的.NET framework 4.0 版。 當重定目標為.NET 4.5，不過，應該完成程式碼檢閱以確定 anyURI 資料型別不做為屬性值應該 （含空格） 無效的 Uri。|
|範圍|次要|
|版本|4.5|
|類型|正在重定目標|

