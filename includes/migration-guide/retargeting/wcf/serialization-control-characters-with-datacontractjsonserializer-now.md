### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>序列化的控制字元的 DataContractJsonSerializer 現在是與 ECMAScript V6 和 V8 相容

|   |   |
|---|---|
|詳細資料|在.NET framework 4.6.2 及更新版本、<xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name>未序列化某些特殊的控制字元，例如 \b \f 和 \t，符合 ECMAScript V6 和 V8 標準相容的方式。 從.NET Framework 4.7，序列化這些控制字元是與 ECMAScript V6 和 V8 相容。|
|建議|針對以.NET Framework 4.7 為目標的應用程式，預設會啟用這項功能。 如果不需要此行為，您可將下列程式行加入至 app.config 或 web.config 檔案的 <code>&lt;runtime&gt;</code> 區段，以選擇退出此功能：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.7|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

