### <a name="rsacng-now-correctly-loads-rsa-keys-of-non-standard-key-size"></a>RSACng 現在正確載入非標準的金鑰大小的 RSA 的金鑰

|   |   |
|---|---|
|詳細資料|在.NET framework 4.6.2 之前，客戶使用非標準的 RSA 憑證的金鑰大小是無法存取這些金鑰透過<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>和<xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=name>擴充方法。  A<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>訊息&quot;不支援要求的金鑰大小&quot;就會擲回。 .NET Framework 4.6.2 中已修正此問題。 同樣地，<xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)>和<xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)>現在使用非標準的金鑰大小，而不擲回<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>s。|
|建議|如果沒有任何例外狀況處理依賴之前行為的邏輯位置<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>就會擲回時使用非標準的金鑰大小，請考慮移除邏輯。|
|範圍|Edge|
|版本|4.6.2|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Security.Cryptography.RSA.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.RSACng.ImportParameters(System.Security.Cryptography.RSAParameters)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPrivateKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li><li><xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey(System.Security.Cryptography.X509Certificates.X509Certificate2)?displayProperty=nameWithType></li></ul>|

