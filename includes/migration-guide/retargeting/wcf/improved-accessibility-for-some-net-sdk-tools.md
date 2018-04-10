### <a name="improved-accessibility-for-some-net-sdk-tools"></a>某些.NET SDK 工具的改良協助工具

|   |   |
|---|---|
|詳細資料|在.NET Framework SDK 4.7.1，解決不同協助工具問題，因而經過改進 svcconfigedit.exe 和 svctraceviewer.exe 工具。 其中大部分是小型的問題，例如未定義的名稱，或者未正確實作某些使用者介面自動化模式。 雖然許多使用者不小心的這些值不正確，使用輔助技術，例如螢幕助讀程式的客戶會發現這些 SDK 工具更容易存取。 當然，這些修正程式變更一些先前的行為，如鍵盤焦點單。若要取得所有這些工具中的協助工具修正程式，您可以下列到 app.config 檔案：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.7.1|
|類型|正在重定目標|

