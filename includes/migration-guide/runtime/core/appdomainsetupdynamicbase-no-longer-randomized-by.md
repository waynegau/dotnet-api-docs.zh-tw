### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a><span data-ttu-id="85da1-101">AppDomainSetup.DynamicBase 不再隨機 UseRandomizedStringHashAlgorithm 由</span><span class="sxs-lookup"><span data-stu-id="85da1-101">AppDomainSetup.DynamicBase is no longer randomized by UseRandomizedStringHashAlgorithm</span></span>

|   |   |
|---|---|
|<span data-ttu-id="85da1-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="85da1-102">Details</span></span>|<span data-ttu-id="85da1-103">在.NET Framework 4.6 的值之前<xref:System.AppDomainSetup.DynamicBase>會隨機處理程序或應用程式定義域之間，如果 UseRandomizedStringHashAlgorithm 已啟用的應用程式組態檔中。</span><span class="sxs-lookup"><span data-stu-id="85da1-103">Prior to the .NET Framework 4.6, the value of <xref:System.AppDomainSetup.DynamicBase> would be randomized between application domains, or between processes, if UseRandomizedStringHashAlgorithm was enabled in the app's config file.</span></span> <span data-ttu-id="85da1-104">從.NET Framework 4.6<xref:System.AppDomainSetup.DynamicBase>不同的應用程式定義域之間，以及應用程式正在執行的不同執行個體之間，會傳回穩定的結果。</span><span class="sxs-lookup"><span data-stu-id="85da1-104">Beginning in the .NET Framework 4.6, <xref:System.AppDomainSetup.DynamicBase> will return a stable result between different instances of an app running, and between different app domains.</span></span> <span data-ttu-id="85da1-105">動態的基底仍會因不同的應用程式。這項變更只會移除相同的應用程式的不同執行個體的隨機命名項目。</span><span class="sxs-lookup"><span data-stu-id="85da1-105">Dynamic bases will still differ for different apps; this change only removes the random naming element for different instances of the same app.</span></span>|
|<span data-ttu-id="85da1-106">建議</span><span class="sxs-lookup"><span data-stu-id="85da1-106">Suggestion</span></span>|<span data-ttu-id="85da1-107">請注意，讓<code>UseRandomizedStringHashAlgorithm</code>不會導致<xref:System.AppDomainSetup.DynamicBase>正在隨機。</span><span class="sxs-lookup"><span data-stu-id="85da1-107">Be aware that enabling <code>UseRandomizedStringHashAlgorithm</code> will not result in <xref:System.AppDomainSetup.DynamicBase> being randomized.</span></span> <span data-ttu-id="85da1-108">如需隨機的基底，必須產生您的應用程式程式碼中，而不是透過此 API。</span><span class="sxs-lookup"><span data-stu-id="85da1-108">If a random base is needed, it must be produced in your app's code rather than via this API.</span></span>|
|<span data-ttu-id="85da1-109">範圍</span><span class="sxs-lookup"><span data-stu-id="85da1-109">Scope</span></span>|<span data-ttu-id="85da1-110">Edge</span><span class="sxs-lookup"><span data-stu-id="85da1-110">Edge</span></span>|
|<span data-ttu-id="85da1-111">版本</span><span class="sxs-lookup"><span data-stu-id="85da1-111">Version</span></span>|<span data-ttu-id="85da1-112">4.6</span><span class="sxs-lookup"><span data-stu-id="85da1-112">4.6</span></span>|
|<span data-ttu-id="85da1-113">類型</span><span class="sxs-lookup"><span data-stu-id="85da1-113">Type</span></span>|<span data-ttu-id="85da1-114">執行階段</span><span class="sxs-lookup"><span data-stu-id="85da1-114">Runtime</span></span>|
|<span data-ttu-id="85da1-115">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="85da1-115">Affected APIs</span></span>|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|
