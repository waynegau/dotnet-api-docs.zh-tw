### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a>IPad 不應在自訂的功能檔案，所以現在瀏覽器功能

|   |   |
|---|---|
|詳細資料|從.NET 4.5 開始，iPad 是識別項在預設 ASP.NET 瀏覽器的功能檔案中，所以不應該使用自訂的功能檔案中|
|建議|如果 iPad 特定功能是必要的則必須以修改 iPad 上預先定義的閘道 refID 設定功能&quot;IPad&quot;而不是透過產生新&quot;IPad&quot;使用者代理程式的識別碼比對。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|

