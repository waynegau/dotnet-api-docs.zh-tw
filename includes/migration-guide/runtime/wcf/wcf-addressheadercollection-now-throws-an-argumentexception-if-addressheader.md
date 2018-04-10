### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>WCF AddressHeaderCollection 現在會擲回 ArgumentException 如果 addressHeader 元素為 null

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.7.1，開始<xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})>建構函式會擲回<xref:System.ArgumentException>如果其中一個項目是<code>null</code>。 在.NET Framework 4.7 和更早版本中，會擲不回任何例外狀況。|
|建議|如果您遇到這項變更.NET Framework 4.7.1 或更新版本上的相容性問題，您可以退出它將下列這一行加入<code>&lt;runtime&gt;</code>app.config 檔的區段::<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|範圍|次要|
|版本|4.7.1|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

