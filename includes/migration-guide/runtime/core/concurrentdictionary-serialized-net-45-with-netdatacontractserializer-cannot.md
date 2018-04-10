### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>使用 NetDataContractSerializer.NET 4.5 中經過序列化 ConcurrentDictionary 無法還原序列化的.NET 4.5.1 或 4.5.2

|   |   |
|---|---|
|詳細資料|因為內部變更為型別，而<xref:System.Collections.Concurrent.ConcurrentDictionary%602>以.NET Framework 4.5 所序列化的物件使用<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>無法還原序列化，在.NET Framework 4.5.1 或.NET Framework 4.5.2.Note 也移動的方向 （中使用.NET Framework 序列化 4.5.x 和還原序列化的.NET Framework 4.5) 的運作方式。 同樣地，.NET Framework 4.6.Serializing 適用於所有 4.x 跨版本的序列化和還原序列化的單一.NET Framework 版本不受影響。|
|建議|如果必須序列化和還原序列化<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name>之間的.NET Framework 4.5 和.NET Framework 4.5.1/4.5.2，要替代的序列化程式<xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name>或<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>應該用於序列化程式，而不是<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>。或者，.NET Framework 4.6 中，解決這個問題，因為它可能解決方法是升級至.NET Framework 的版本。|
|範圍|次要|
|版本|4.5.1|
|類型|執行階段|

