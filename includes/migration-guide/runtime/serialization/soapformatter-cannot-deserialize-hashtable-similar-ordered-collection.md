### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter 無法還原序列化雜湊表及類似排序的集合物件

|   |   |
|---|---|
|詳細資料|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name>保證物件序列化在一個.NET Framework 版本將會成功還原序列化的不同版本的作用。 具體來說，某些已排序集合 (例如<xref:System.Collections.Hashtable?displayProperty=name>) 4.0 和 4.5 之間的成員，這些型別的物件無法還原序列化.NET 4.0 如果序列化.NET 4.5 加入。 請注意，如果序列化資料以相同的 .NET Framework 版本序列化和還原序列化，就不會發生任何問題。|
|建議|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> 應該取代成序列化<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>序列化或<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>處理.NET Framework 變更的彈性。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

