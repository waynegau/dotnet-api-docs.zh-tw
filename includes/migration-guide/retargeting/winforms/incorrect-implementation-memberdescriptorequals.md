### <a name="incorrect-implementation-of-memberdescriptorequals"></a>不正確實作 MemberDescriptor.Equals

|   |   |
|---|---|
|詳細資料|原始實作&quot;等於&quot;方法比較兩個不同的字串屬性，從下比較的物件： 類別名稱，以描述字串。 修正方法是比較&quot;類別&quot;要第一個物件的&quot;類別&quot;為第二個和&quot;描述&quot;至&quot;描述&quot;。 為退出新的行為，如果目標 4.6.2 true 或 false 來啟用此修正程式，當目標 framework 版本低於 4.6.2 時，可以設定 MemberDescriptorEqualsReturnsFalseIfEquivalent 組態值。|
|建議|如果您的應用程式相依於 MemberDescriptor.Equals 有時會傳回 false 當描述元是相等的而且您目標設定 4.6.2 版本的.NET Framework 中，您有數個選項：<ol><li>要比較的程式碼變更&quot;類別&quot;和&quot;描述&quot;手動除了執行 Equals 方法的欄位。</li><li>選擇退出這項變更加入 app.config 檔案中的下列值：</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>如果您的應用程式的目標 4.6.1 或較低版本的.NET Framework 中，而且您想要啟用這項變更，您可以設定為 false 的相容性參數加入 app.config 檔案中的下列值：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.6.2|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

