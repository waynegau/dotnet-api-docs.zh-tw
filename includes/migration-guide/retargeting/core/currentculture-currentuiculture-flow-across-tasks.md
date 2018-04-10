### <a name="currentculture-and-currentuiculture-flow-across-tasks"></a>CurrentCulture 和 CurrentUICulture 流經工作

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.6<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>和<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>會儲存在執行緒的<xref:System.Threading.ExecutionContext?displayProperty=name>，其中非同步作業之間流動。這表示變更<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>或<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>會反映在稍後以非同步方式執行的工作。 這點不同於舊版.NET Framework 的行為 (這會重設<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>和<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>中所有的非同步工作)。|
|建議|此變更影響的應用程式可能會解決它明確地設定所需<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>或<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>非同步工作中的第一個作業。 或者，舊的行為 (不讓獲得<xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) 可能會選擇加入，藉由設定下列相容性參數：<pre><code class="language-C#">AppContext.SetSwitch(&quot;Switch.System.Globalization.NoAsyncCurrentCulture&quot;, true);&#13;&#10;</code></pre>Wpf 在.NET Framework 4.6.2 已修正此問題。 它也已修正在.NET Framework 4.6，透過 4.6.1 [KB 3139549](https://support.microsoft.com/kb/3139549)。 目標為.NET 4.6 或更新版本的應用程式將自動取得正確的行為在 WPF 應用程式- <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) 會在發送器作業之間保留。|
|範圍|次要|
|版本|4.6|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentUICulture?displayProperty=nameWithType></li></ul>|

