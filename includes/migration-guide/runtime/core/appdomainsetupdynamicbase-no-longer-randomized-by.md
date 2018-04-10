### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>AppDomainSetup.DynamicBase 不再隨機 UseRandomizedStringHashAlgorithm 由

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.6 的值之前<xref:System.AppDomainSetup.DynamicBase>會隨機處理程序或應用程式定義域之間，如果 UseRandomizedStringHashAlgorithm 已啟用的應用程式組態檔中。 從.NET Framework 4.6<xref:System.AppDomainSetup.DynamicBase>不同的應用程式定義域之間，以及應用程式正在執行的不同執行個體之間，會傳回穩定的結果。 動態的基底仍會因不同的應用程式。這項變更只會移除相同的應用程式的不同執行個體的隨機命名項目。|
|建議|請注意，讓<code>UseRandomizedStringHashAlgorithm</code>不會導致<xref:System.AppDomainSetup.DynamicBase>正在隨機。 如需隨機的基底，必須產生您的應用程式程式碼中，而不是透過此 API。|
|範圍|Edge|
|版本|4.6|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

