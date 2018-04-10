### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>NetDataContractSerializer 無法還原序列化序列化並以不同的.NET 版本 ConcurrentDictionary

|   |   |
|---|---|
|詳細資料|根據設計，<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>序列化和還原序列化兩端共用相同的 CLR 型別時，才可以使用。 因此，不保證可以在不同版本還原序列化某一個.NET Framework 版本與序列化的物件。<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> 是已知的不可以將還原序列化正確如果序列化的.NET Framework 4.5 或更早版本和還原序列化以.NET Framework 4.5.1 或更新版本的類型。|
|建議|有許多的可能解決方案此問題：<ul><li>若要使用.NET Framework 4.5.1，以及序列化的電腦升級。</li><li>使用<xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name>而不是<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>因為這不預期會有完全相同 CLR 型別在序列化和還原序列化兩端。</li><li>使用<xref:System.Collections.Generic.Dictionary%602?displayProperty=name>而不是<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name>因為它不會呈現此特定 4.5-&gt;4.5.1 中斷。</li></ul>|
|範圍|次要|
|版本|4.5.1|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

