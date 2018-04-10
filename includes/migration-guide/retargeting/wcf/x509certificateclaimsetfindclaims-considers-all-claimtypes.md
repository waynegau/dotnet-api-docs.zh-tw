### <a name="x509certificateclaimsetfindclaims-considers-all-claimtypes"></a>X509CertificateClaimSet.FindClaims 會考慮所有 claimTypes

|   |   |
|---|---|
|詳細資料|應用程式中的目標.NET Framework 4.6.1 中，如果 X509 宣告集初始化自 SAN 欄位中有多個 DNS 項目憑證<xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name>方法會嘗試比對的 claimType 引數，使用所有 DNS 項目。若是以舊版.NET Framework 中，目標的應用程式<xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=name>方法會嘗試比對的 claimType 引數，只會使用最後一個 DNS 項目。|
|建議|這項變更只會影響以 .NET Framework 4.6.1 為目標的應用程式。 您可以使用 [DisableMultipleDNSEntries](~/docs/framework/migration-guide/mitigation-x509certificateclaimset-findclaims-method.md#mitigation) 相容性參數來停用這項變更 (如果以 4.6.1 以前版本為目標則可啟用)。|
|範圍|次要|
|版本|4.6.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.IdentityModel.Claims.X509CertificateClaimSet.FindClaims(System.String,System.String)?displayProperty=nameWithType></li></ul>|

