### <a name="encoderparameter-ctor-is-obsolete"></a><span data-ttu-id="d9b02-101">EncoderParameter ctor 已過時</span><span class="sxs-lookup"><span data-stu-id="d9b02-101">EncoderParameter ctor is obsolete</span></span>

|   |   |
|---|---|
|<span data-ttu-id="d9b02-102">詳細資料</span><span class="sxs-lookup"><span data-stu-id="d9b02-102">Details</span></span>|<span data-ttu-id="d9b02-103"><xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> 建構函式現在已淘汰，如果使用，就會產生建置警告。</span><span class="sxs-lookup"><span data-stu-id="d9b02-103">The <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)> constructor is obsolete now and will introduce build warnings if used.</span></span>|
|<span data-ttu-id="d9b02-104">建議</span><span class="sxs-lookup"><span data-stu-id="d9b02-104">Suggestion</span></span>|<span data-ttu-id="d9b02-105">雖然<xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>建構函式將繼續運作，應該改為使用下列建構函式，以避免重新編譯使用.NET 4.5 工具的程式碼時的過時的建置警告： <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>。</span><span class="sxs-lookup"><span data-stu-id="d9b02-105">Although the <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)>constructor will continue to work, the following constructor should be used instead to avoid the obsolete build warning when re-compiling code with .NET 4.5 tools: <xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Drawing.Imaging.EncoderParameterValueType,System.IntPtr)>.</span></span>|
|<span data-ttu-id="d9b02-106">範圍</span><span class="sxs-lookup"><span data-stu-id="d9b02-106">Scope</span></span>|<span data-ttu-id="d9b02-107">次要</span><span class="sxs-lookup"><span data-stu-id="d9b02-107">Minor</span></span>|
|<span data-ttu-id="d9b02-108">版本</span><span class="sxs-lookup"><span data-stu-id="d9b02-108">Version</span></span>|<span data-ttu-id="d9b02-109">4.5</span><span class="sxs-lookup"><span data-stu-id="d9b02-109">4.5</span></span>|
|<span data-ttu-id="d9b02-110">類型</span><span class="sxs-lookup"><span data-stu-id="d9b02-110">Type</span></span>|<span data-ttu-id="d9b02-111">正在重定目標</span><span class="sxs-lookup"><span data-stu-id="d9b02-111">Retargeting</span></span>|
|<span data-ttu-id="d9b02-112">受影響的 API</span><span class="sxs-lookup"><span data-stu-id="d9b02-112">Affected APIs</span></span>|<ul><li><xref:System.Drawing.Imaging.EncoderParameter.%23ctor(System.Drawing.Imaging.Encoder,System.Int32,System.Int32,System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|
