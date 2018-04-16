### <a name="cspparametersparentwindowhandle-now-expects-hwnd-value"></a><span data-ttu-id="b1b9b-101">CspParameters.ParentWindowHandle 現在必須要有的 HWND 值</span><span class="sxs-lookup"><span data-stu-id="b1b9b-101">CspParameters.ParentWindowHandle now expects HWND value</span></span>

|   |   |
|---|---|
|<span data-ttu-id="b1b9b-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="b1b9b-102">Details</span></span>|<span data-ttu-id="b1b9b-103"><xref:System.Security.Cryptography.CspParameters.ParentWindowHandle>在.NET Framework 2.0 中，導入的值，可讓應用程式註冊父視窗控制代碼值，以便存取金鑰所需的任何 UI （例如 PIN 提示或同意對話方塊） 做為強制回應的子系至指定的視窗隨即開啟。從目標為.NET Framework 4.7 應用程式開始，Windows Form 應用程式可以設定<xref:System.Security.Cryptography.CspParameters.ParentWindowHandle>屬性具有類似下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="b1b9b-103">The <xref:System.Security.Cryptography.CspParameters.ParentWindowHandle> value, introduced in .NET Framework 2.0, allows an application to register a parent window handle value such that any UI required to access the key (such as a PIN prompt or consent dialog) opens as a modal child to the specified window.Starting with apps that target the .NET Framework 4.7, a Windows Forms application can set the <xref:System.Security.Cryptography.CspParameters.ParentWindowHandle> property with code like the following:</span></span><pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre><span data-ttu-id="b1b9b-104">在舊版的.NET Framework 中，值必須為<xref:System.IntPtr?displayProperty=name>代表記憶體中的位置其中[HWND](https://msdn.microsoft.com/library/windows/desktop/aa383751.aspx#HWND)存放的值。</span><span class="sxs-lookup"><span data-stu-id="b1b9b-104">In previous versions of the .NET Framework, the value was expected to be an <xref:System.IntPtr?displayProperty=name> representing a location in memory where the [HWND](https://msdn.microsoft.com/library/windows/desktop/aa383751.aspx#HWND) value resided.</span></span> <span data-ttu-id="b1b9b-105">將屬性設定為表單。在 Windows 7 上處理和更早版本沒有任何作用中，但在 Windows 8 和更新版本，則會導致&quot; <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>： 參數不正確。&quot;</span><span class="sxs-lookup"><span data-stu-id="b1b9b-105">Setting the property to form.Handle on Windows 7 and earlier versions had no effect, but on Windows 8 and later versions, it results in a &quot;<xref:System.Security.Cryptography.CryptographicException?displayProperty=name>: The parameter is incorrect.&quot;</span></span>|
|<span data-ttu-id="b1b9b-106">建議</span><span class="sxs-lookup"><span data-stu-id="b1b9b-106">Suggestion</span></span>|<span data-ttu-id="b1b9b-107">若要使用簡化的形式建議應用程式為目標.NET 4.7 或更高版本與想要註冊的父視窗關聯性：</span><span class="sxs-lookup"><span data-stu-id="b1b9b-107">Applications targeting .NET 4.7 or higher wishing to register a parent window relationship are encouraged to use the simplified form:</span></span><pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre><span data-ttu-id="b1b9b-108">使用者已識別正確的值來傳遞已持有值記憶體位置的位址<code>form.Handle</code>即可退出藉由設定 AppContext 參數的行為變更<code>Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle</code>至<code>true</code>。</span><span class="sxs-lookup"><span data-stu-id="b1b9b-108">Users who had identified that the correct value to pass was the address of a memory location which held the value <code>form.Handle</code> can opt out of the behavior change by setting the AppContext switch <code>Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle</code> to <code>true</code>.</span></span><ol><li><span data-ttu-id="b1b9b-109">程式以程式設計方式設定 compat 切換 AppContext 上所述[這裡](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</span><span class="sxs-lookup"><span data-stu-id="b1b9b-109">By programmatically setting compat switches on the AppContext, as explained [here](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</span></span></li><li><span data-ttu-id="b1b9b-110">將下列程式行加入至 app.config 檔案的 <code>&lt;runtime&gt;</code> 區段：</span><span class="sxs-lookup"><span data-stu-id="b1b9b-110">By adding the following line to the <code>&lt;runtime&gt;</code> section of the app.config file:</span></span></li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="b1b9b-111">相反地，使用者想要選擇加入新行為對.NET Framework 4.7 執行階段時載入在舊版.NET Framework 的應用程式可以設定 AppContext 切換至<code>false</code>。</span><span class="sxs-lookup"><span data-stu-id="b1b9b-111">Conversely, users who wish to opt in to the new behavior on the .NET Framework 4.7 runtime when the application loads under older .NET Framework versions can set the AppContext switch to <code>false</code>.</span></span>|
|<span data-ttu-id="b1b9b-112">範圍</span><span class="sxs-lookup"><span data-stu-id="b1b9b-112">Scope</span></span>|<span data-ttu-id="b1b9b-113">次要</span><span class="sxs-lookup"><span data-stu-id="b1b9b-113">Minor</span></span>|
|<span data-ttu-id="b1b9b-114">版本</span><span class="sxs-lookup"><span data-stu-id="b1b9b-114">Version</span></span>|<span data-ttu-id="b1b9b-115">4.7</span><span class="sxs-lookup"><span data-stu-id="b1b9b-115">4.7</span></span>|
|<span data-ttu-id="b1b9b-116">類型</span><span class="sxs-lookup"><span data-stu-id="b1b9b-116">Type</span></span>|<span data-ttu-id="b1b9b-117">正在重定目標</span><span class="sxs-lookup"><span data-stu-id="b1b9b-117">Retargeting</span></span>|
|<span data-ttu-id="b1b9b-118">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="b1b9b-118">Affected APIs</span></span>|<ul><li><xref:System.Security.Cryptography.CspParameters.ParentWindowHandle?displayProperty=nameWithType></li></ul>|
