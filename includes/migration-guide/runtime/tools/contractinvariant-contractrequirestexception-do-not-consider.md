### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant 或 Contract.Requires<TException>不會考慮要純 String.IsNullOrEmpty

|   |   |
|---|---|
|詳細資料|目標.NET Framework 4.6.1 中，如果非變異合約的應用程式的<xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType>或前置條件合約<xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)>呼叫<xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType>方法，重寫器會發出編譯器警告 CC1036:&quot;偵測到呼叫方法 'System.String.IsNullOrWhteSpace(System.String)' 沒有 [純粹] 方法中。&quot;這是編譯器警告，而不編譯器錯誤。|
|建議|[GitHub 問題 #339](https://github.com/Microsoft/CodeContracts/issues/339) 中已解決這種行為。 若要消除這則警告，您可以下載並編譯的程式碼合約工具的原始程式碼的更新的版本[GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md)。 您可以在頁面底部找到下載資訊。|
|範圍|次要|
|版本|4.6.1|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

