### <a name="default-value-of-servicepointmanagersecurityprotocol-is-securityprotocoltypesystemdefault"></a>ServicePointManager.SecurityProtocol 的預設值是 SecurityProtocolType.System.Default

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.7 的預設值為目標的應用程式開始<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>屬性是<xref:System.Net.SecurityProtocolType.SystemDefault?displayProperty=nameWithType>。 這項變更可以讓網路應用程式開發介面繼承作業系統，而不要使用硬式編碼的值，由.NET Framework 定義的預設安全性通訊協定為基礎 （例如 FTP、 HTTPS 及 SMTP） SslStream 的.NET Framework。 預設會依作業系統和系統管理員執行任何自訂設定而異。 如需每個 Windows 作業系統版本中的預設安全通道通訊協定資訊，請參閱[中 TLS/SSL (安全通道 SSP) 的通訊協定](https://msdn.microsoft.com/library/windows/desktop/mt808159.aspx)。目標是舊版的.NET Framework 中，預設值的應用程式<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>屬性的目標.NET framework 版本而定。 請參閱[網路區段的重定目標變更從.NET Framework 4.5.2 到 4.6 移轉](~/docs/framework/migration-guide/retargeting/4.5.2-4.6.md#networking)如需詳細資訊。|
|建議|這項變更會影響以.NET Framework 4.7 或更新版本為目標的應用程式。如果您想要使用定義的通訊協定，而不是依賴系統預設值，您可以明確設定的值<xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType>屬性。如果不需要這項變更，您可以藉由新增組態設定，來選擇不使用[\<執行階段 >](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)應用程式組態檔的區段。 下列範例會顯示<code>&lt;runtime&gt;</code>區段和<code>Switch.System.Net.DontEnableSystemDefaultTlsVersions</code>退出交換器：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSystemDefaultTlsVersions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Net.ServicePointManager.SecurityProtocol?displayProperty=nameWithType></li></ul>|

