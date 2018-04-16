### <a name="unicode-standard-version-80-categories-now-supported"></a><span data-ttu-id="fa0a6-101">現在支援 Unicode 標準 8.0 版類別</span><span class="sxs-lookup"><span data-stu-id="fa0a6-101">Unicode standard version 8.0 categories now supported</span></span>

|   |   |
|---|---|
|<span data-ttu-id="fa0a6-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="fa0a6-102">Details</span></span>|<span data-ttu-id="fa0a6-103">在.NET Framework 4.6.2 framework 中的 Unicode 資料已升級從 Unicode 標準 6.3 版至 8.0 版。</span><span class="sxs-lookup"><span data-stu-id="fa0a6-103">In .NET Framework 4.6.2, Unicode data in the framework has been upgraded from Unicode standard version 6.3 to version 8.0.</span></span>  <span data-ttu-id="fa0a6-104">當.NET Framework 4.6.2 中的 Unicode 字元分類要求時，某些結果可能不符合舊版的.NET Framework 中的結果。</span><span class="sxs-lookup"><span data-stu-id="fa0a6-104">When requesting Unicode character category in .NET Framework 4.6.2, some results might not match the results in previous .NET Framework versions.</span></span>  <span data-ttu-id="fa0a6-105">這項變更通常會影響 Cherokee 音節和新的 Ta1 Lue 母音符號和音調標記。</span><span class="sxs-lookup"><span data-stu-id="fa0a6-105">This change mostly affects Cherokee syllables and New Tai Lue vowels signs and tone marks.</span></span>|
|<span data-ttu-id="fa0a6-106">建議</span><span class="sxs-lookup"><span data-stu-id="fa0a6-106">Suggestion</span></span>|<span data-ttu-id="fa0a6-107">檢閱程式碼，並移除/變更邏輯取決於硬式編碼的 Unicode 字元分類。</span><span class="sxs-lookup"><span data-stu-id="fa0a6-107">Review code and remove/change logic that depends on hard-coded Unicode character categories.</span></span>|
|<span data-ttu-id="fa0a6-108">範圍</span><span class="sxs-lookup"><span data-stu-id="fa0a6-108">Scope</span></span>|<span data-ttu-id="fa0a6-109">次要</span><span class="sxs-lookup"><span data-stu-id="fa0a6-109">Minor</span></span>|
|<span data-ttu-id="fa0a6-110">版本</span><span class="sxs-lookup"><span data-stu-id="fa0a6-110">Version</span></span>|<span data-ttu-id="fa0a6-111">4.6.2</span><span class="sxs-lookup"><span data-stu-id="fa0a6-111">4.6.2</span></span>|
|<span data-ttu-id="fa0a6-112">類型</span><span class="sxs-lookup"><span data-stu-id="fa0a6-112">Type</span></span>|<span data-ttu-id="fa0a6-113">執行階段</span><span class="sxs-lookup"><span data-stu-id="fa0a6-113">Runtime</span></span>|
|<span data-ttu-id="fa0a6-114">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="fa0a6-114">Affected APIs</span></span>|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|
