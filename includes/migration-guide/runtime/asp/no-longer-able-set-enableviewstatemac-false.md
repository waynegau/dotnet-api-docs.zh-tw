### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>不再能夠 EnableViewStateMac 設為 false

|   |   |
|---|---|
|詳細資料|ASP.NET 不再允許開發人員指定 <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> 或 <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>。 檢視狀態訊息驗證碼 (MAC) 現在會強制所有要求內嵌檢視狀態。 明確將 EnableViewStateMac 屬性設定為應用程式<code>false</code>會受到影響。|
|建議|EnableViewStateMac 必須假設為 true，和任何產生的 MAC 錯誤，必須先解析 (如所述[本指南](https://support.microsoft.com/kb/2915218)，其中包含多個解決方式視 MAC 錯誤造成的細節而定)。|
|範圍|主要|
|版本|4.5.2|
|類型|執行階段|

