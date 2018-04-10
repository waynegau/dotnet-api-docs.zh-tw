### <a name="workflow-checksums-changed-from-md5-to-sha1"></a>工作流程從 MD5 變更為 SHA1 的總和檢查碼

|   |   |
|---|---|
|詳細資料|若要支援使用 Visual Studio 偵錯，工作流程執行階段會產生使用雜湊演算法的工作流程執行個體的總和檢查碼。 在.NET Framework 4.6.2 和更早版本中，工作流程的總和檢查碼雜湊使用 MD5 演算法，啟用 FIPS 的系統上造成問題。 從.NET Framework 4.7，此演算法是 SHA1。 如果您的程式碼已保存這些總和檢查碼，就會不相容。|
|建議|如果您的程式碼無法載入工作流程執行個體，因為總和檢查碼失敗，請嘗試設定<code>AppContext</code>切換&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;為 true。在程式碼：<pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre>或在組態中：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7|
|類型|正在重定目標|

