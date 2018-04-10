### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash 現在會傳回 False 的任何電腦驗證失敗

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.6.2 開始，這個方法會傳回<strong>False</strong>如果簽章本身的格式不正確。 它現在會傳回 false 的任何電腦驗證失敗。在.NET Framework 4.6 和 4.6.1，方法會擲回<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>如果簽章本身的格式不正確。|
|建議|處理取決於其執行的任何程式碼<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>應該改為執行，如果驗證失敗而且方法會傳回<strong>False</strong>。|
|範圍|次要|
|版本|4.6.2|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

