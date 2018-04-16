### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a><span data-ttu-id="ec93d-101">WCF MsmqSecureHashAlgorithm 預設值現在是 SHA256</span><span class="sxs-lookup"><span data-stu-id="ec93d-101">WCF MsmqSecureHashAlgorithm default value is now SHA256</span></span>

|   |   |
|---|---|
|<span data-ttu-id="ec93d-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="ec93d-102">Details</span></span>|<span data-ttu-id="ec93d-103">從.NET Framework 4.7.1 開始，預設的訊息簽章在 WCF 中的 Msmq 訊息的演算法是 SHA256。</span><span class="sxs-lookup"><span data-stu-id="ec93d-103">Starting with the .NET Framework 4.7.1, the default message signing algorithm in WCF for Msmq messages is SHA256.</span></span> <span data-ttu-id="ec93d-104">在.NET Framework 4.7 和更早版本中，預設的訊息簽章演算法是 SHA1。</span><span class="sxs-lookup"><span data-stu-id="ec93d-104">In the .NET Framework 4.7 and earlier versions, the default message signing algorithm is SHA1.</span></span>|
|<span data-ttu-id="ec93d-105">建議</span><span class="sxs-lookup"><span data-stu-id="ec93d-105">Suggestion</span></span>|<span data-ttu-id="ec93d-106">如果在.NET Framework 4.7.1 上執行這項變更的相容性問題或更新版本中，您可以退出變更將下列這一行加入<code>&lt;runtime&gt;</code>app.config 檔的區段：</span><span class="sxs-lookup"><span data-stu-id="ec93d-106">If you run into compatibility issues with this change on the .NET Framework 4.7.1 or later, you can opt-out the change by adding the following line to the <code>&lt;runtime&gt;</code>section of your app.config file:</span></span><pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="ec93d-107">範圍</span><span class="sxs-lookup"><span data-stu-id="ec93d-107">Scope</span></span>|<span data-ttu-id="ec93d-108">次要</span><span class="sxs-lookup"><span data-stu-id="ec93d-108">Minor</span></span>|
|<span data-ttu-id="ec93d-109">版本</span><span class="sxs-lookup"><span data-stu-id="ec93d-109">Version</span></span>|<span data-ttu-id="ec93d-110">4.7.1</span><span class="sxs-lookup"><span data-stu-id="ec93d-110">4.7.1</span></span>|
|<span data-ttu-id="ec93d-111">類型</span><span class="sxs-lookup"><span data-stu-id="ec93d-111">Type</span></span>|<span data-ttu-id="ec93d-112">執行階段</span><span class="sxs-lookup"><span data-stu-id="ec93d-112">Runtime</span></span>|
