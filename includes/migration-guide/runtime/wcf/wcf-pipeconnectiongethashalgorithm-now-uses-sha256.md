### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF PipeConnection.GetHashAlgorithm 現在會使用 SHA256

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.7.1 開始，Windows Communication Foundation 會使用 SHA256 雜湊產生隨機的具名管道的名稱。 在.NET Framework 4.7 和更早版本中，它會使用 SHA1 雜湊。|
|建議|如果您進行這項變更的相容性問題到.NET Framework 上執行 4.7.1 或更新版本中，您可以選擇不使用它將下列這一行加入<code>&lt;runtime&gt;</code>app.config 檔的區段：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7.1|
|類型|執行階段|

