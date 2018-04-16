### <a name="throttle-concurrent-requests-per-session"></a><span data-ttu-id="346ba-101">每一個工作階段的節流閥並行要求數目</span><span class="sxs-lookup"><span data-stu-id="346ba-101">Throttle concurrent requests per session</span></span>

|   |   |
|---|---|
|<span data-ttu-id="346ba-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="346ba-102">Details</span></span>|<span data-ttu-id="346ba-103">.NET Framework 4.6.2 中更早版本，ASP.NET，循序執行使用相同的 Sessionid 的要求，ASP.NET 一律會透過 cookie Sessionid 發出預設。</span><span class="sxs-lookup"><span data-stu-id="346ba-103">In the .NET Framework 4.6.2 and earlier, ASP.NET executes requests with the same Sessionid sequentially, and ASP.NET always issues the Sessionid through cookies by default.</span></span> <span data-ttu-id="346ba-104">如果頁面會花很長的時間來回應，它將會大幅降低伺服器效能，只要在瀏覽器上按 F5。</span><span class="sxs-lookup"><span data-stu-id="346ba-104">If a page takes a long time to respond, it will significantly degrade server performance just by pressing F5 on the browser.</span></span> <span data-ttu-id="346ba-105">在修正，我們加入了計數器來追蹤要求排入佇列，並終止要求時超過指定的限制。</span><span class="sxs-lookup"><span data-stu-id="346ba-105">In the fix, we added a counter to track the queued requests and terminate the requests when they exceed a specified limit.</span></span> <span data-ttu-id="346ba-106">預設值為 50。</span><span class="sxs-lookup"><span data-stu-id="346ba-106">The default value is 50.</span></span> <span data-ttu-id="346ba-107">如果達到限制時，警告將會記錄到事件記錄及 HTTP 500 回應可能會在 IIS 記錄檔中記錄中。</span><span class="sxs-lookup"><span data-stu-id="346ba-107">If the limit is reached, a warning will be logged in the event log, and an HTTP 500 response may be recorded in the IIS log.</span></span>|
|<span data-ttu-id="346ba-108">建議</span><span class="sxs-lookup"><span data-stu-id="346ba-108">Suggestion</span></span>|<span data-ttu-id="346ba-109">若要還原舊行為，您可以將下列設定加入您的 web.config 檔案以選擇退出新行為。</span><span class="sxs-lookup"><span data-stu-id="346ba-109">To restore the old behavior, you can add the following setting to your web.config file to opt out of the new behavior.</span></span><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;aspnet:RequestQueueLimitPerSession&quot; value=&quot;2147483647&quot;/&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="346ba-110">範圍</span><span class="sxs-lookup"><span data-stu-id="346ba-110">Scope</span></span>|<span data-ttu-id="346ba-111">Edge</span><span class="sxs-lookup"><span data-stu-id="346ba-111">Edge</span></span>|
|<span data-ttu-id="346ba-112">版本</span><span class="sxs-lookup"><span data-stu-id="346ba-112">Version</span></span>|<span data-ttu-id="346ba-113">4.7</span><span class="sxs-lookup"><span data-stu-id="346ba-113">4.7</span></span>|
|<span data-ttu-id="346ba-114">類型</span><span class="sxs-lookup"><span data-stu-id="346ba-114">Type</span></span>|<span data-ttu-id="346ba-115">正在重定目標</span><span class="sxs-lookup"><span data-stu-id="346ba-115">Retargeting</span></span>|
