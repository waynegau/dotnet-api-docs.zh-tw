### <a name="cspparametersparentwindowhandle-now-expects-hwnd-value"></a>CspParameters.ParentWindowHandle 現在必須要有的 HWND 值

|   |   |
|---|---|
|詳細資料|<xref:System.Security.Cryptography.CspParameters.ParentWindowHandle>在.NET Framework 2.0 中，導入的值，可讓應用程式註冊父視窗控制代碼值，以便存取金鑰所需的任何 UI （例如 PIN 提示或同意對話方塊） 做為強制回應的子系至指定的視窗隨即開啟。從目標為.NET Framework 4.7 應用程式開始，Windows Form 應用程式可以設定<xref:System.Security.Cryptography.CspParameters.ParentWindowHandle>屬性具有類似下列程式碼：<pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre>在舊版的.NET Framework 中，值必須為<xref:System.IntPtr?displayProperty=name>代表記憶體中的位置其中[HWND](https://msdn.microsoft.com/library/windows/desktop/aa383751.aspx#HWND)存放的值。 將屬性設定為表單。在 Windows 7 上處理和更早版本沒有任何作用中，但在 Windows 8 和更新版本，則會導致&quot; <xref:System.Security.Cryptography.CryptographicException?displayProperty=name>： 參數不正確。&quot;|
|建議|若要使用簡化的形式建議應用程式為目標.NET 4.7 或更高版本與想要註冊的父視窗關聯性：<pre><code class="language-C#">cspParameters.ParentWindowHandle = form.Handle;&#13;&#10;</code></pre>使用者已識別正確的值來傳遞已持有值記憶體位置的位址<code>form.Handle</code>即可退出藉由設定 AppContext 參數的行為變更<code>Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle</code>至<code>true</code>。<ol><li>程式以程式設計方式設定 compat 切換 AppContext 上所述[這裡](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>將下列程式行加入至 app.config 檔案的 <code>&lt;runtime&gt;</code> 區段：</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.DoNotAddrOfCspParentWindowHandle=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>相反地，使用者想要選擇加入新行為對.NET Framework 4.7 執行階段時載入在舊版.NET Framework 的應用程式可以設定 AppContext 切換至<code>false</code>。|
|範圍|次要|
|版本|4.7|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Security.Cryptography.CspParameters.ParentWindowHandle?displayProperty=nameWithType></li></ul>|

