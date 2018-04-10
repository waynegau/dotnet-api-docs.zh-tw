### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>MaxRequestLength 或 maxReceivedMessageSize 的錯誤碼是不同

|   |   |
|---|---|
|詳細資料|訊息在 WCF web 服務裝載於網際網路資訊服務 (IIS) 或 ASP.NET 程式開發伺服器超過 maxRequestLength （在 ASP.NET 中) 或 （在 WCF 中) 的 maxReceivedMessageSize 有不同的錯誤 codeThe HTTP 狀態碼已從 400 （不正確的要求) 413 （要求實體太大），和 maxRequestLength 或 maxReceivedMessageSize 設定超過的訊息會擲回<xref:System.ServiceModel.ProtocolException?displayProperty=name>例外狀況。 這包括串流傳輸模式時的情況。|
|建議|這項變更有助於在訊息長度超過 ASP.NET 或 WCF 所允許之限制的情況下偵錯。您必須修改任何依據 HTTP 400 狀態碼執行處理的程式碼。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|

