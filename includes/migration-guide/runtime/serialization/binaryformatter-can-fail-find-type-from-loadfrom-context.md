### <a name="binaryformatter-can-fail-to-find-type-from-loadfrom-context"></a>BinaryFormatter 可能會失敗，找不到類型從 LoadFrom 內容

|   |   |
|---|---|
|詳細資料|.NET Framework 4.5 的數目為準，<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>變更可能會造成在還原序列化期間的差異，當使用<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>還原序列化具有已 LoadFrom 內容載入的型別。 這些變更是由於新方法<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>立即載入的類型，這會導致不同的行為時<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>會嘗試為該類型在稍後還原序列化。 預設序列化繫結器不會自動搜尋 LoadFrom 內容中，雖然曾經在某些情況下，根據舊的 XmlSerializer 行為。 由於變更，在不同的內容中，載入之組件載入的型別時<xref:System.IO.FileNotFoundException?displayProperty=name>可能會擲回。|
|建議|如果看到這個例外狀況是，<code>Binder</code>屬性<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>可以設定為自訂繫結器，來尋找正確的型別。<pre><code class="language-C#">var formatter = new BinaryFormatter { Binder = new TypeFinderBinder() }&#13;&#10;</code></pre>然後在自訂繫結：<pre><code class="language-C#">public class TypeFinderBinder : SerializationBinder&#13;&#10;{&#13;&#10;private static readonly string s_assemblyName = Assembly.GetExecutingAssembly().FullName;&#13;&#10;&#13;&#10;public override Type BindToType(string assemblyName, string typeName)&#13;&#10;{&#13;&#10;return Type.GetType(String.Format(CultureInfo.InvariantCulture, &quot;{0}, {1}&quot;, typeName, s_assemblyName));&#13;&#10;}&#13;&#10;}&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

