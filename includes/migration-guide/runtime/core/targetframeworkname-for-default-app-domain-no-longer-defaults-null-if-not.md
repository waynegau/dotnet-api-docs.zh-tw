### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>預設應用程式定義域的 TargetFrameworkName 不再預設值為 null，如果未設定

|   |   |
|---|---|
|詳細資料|<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name>先前中為 null 的預設應用程式定義域，除非明確設定。 自 4.6 起<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name>預設應用程式定義域的屬性會有預設值衍生自 TargetFrameworkAttribute，（如果有的話）。 將繼續在非預設應用程式定義域繼承其<xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name>來自預設應用程式定義域 （這將會預設為 null 4.6） 除非明確覆寫。|
|建議|您應該更新程式碼，讓 <xref:System.AppDomainSetup.TargetFrameworkName> 不會預設為 Null。 如果此屬性必須繼續評估為 Null，則可以將它明確設定為該值。|
|範圍|Edge|
|版本|4.6|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

