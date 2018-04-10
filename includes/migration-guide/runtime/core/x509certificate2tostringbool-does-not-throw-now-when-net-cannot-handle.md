### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) 不會擲回現在當.NET 無法處理的憑證

|   |   |
|---|---|
|詳細資料|先前，這個方法會擲回<code>true</code>已為參數傳遞的詳細資訊，並出現 %未支援的.NET Framework 安裝憑證。 現在，方法將會成功，並傳回省略了的憑證無法存取部分的有效字串。|
|建議|取決於任何程式碼<xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)>應該更新為在某些情況下，API 會有先前擲回預期會傳回的字串，可能會排除部分的憑證資料 （例如公開金鑰、 私用金鑰和擴充功能）。|
|範圍|Edge|
|版本|4.6|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

