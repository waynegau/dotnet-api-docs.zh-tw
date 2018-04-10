### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>例外狀況處理程式碼從 ImageSourceConverter.ConvertFrom NullReferenceException

|   |   |
|---|---|
|詳細資料|例外狀況處理程式碼中的錯誤<xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)>造成不正確<xref:System.NullReferenceException?displayProperty=name>擲回，而不是預期的例外狀況 (例如<xref:System.IO.DirectoryNotFoundException?displayProperty=name>， <xref:System.IO.FileNotFoundException?displayProperty=name>)，這項變更，讓該方法現在會擲回正確的例外狀況，請修正該錯誤。藉由預設目標為.NET Framework 4.6.2 的所有應用程式和以下仍將會擲回<xref:System.NullReferenceException?displayProperty=name>和更新版本相容性，目標為.NET Framework 4.7 的開發人員應該會看到正確 exceptions.// 取代的 'x' 的空間的話|
|建議|開發人員想要還原成取得<xref:System.NullReferenceException?displayProperty=name>當目標為.NET Framework 4.7 可以加入/合併至他們的應用程式的 App.config 檔下：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.7|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

