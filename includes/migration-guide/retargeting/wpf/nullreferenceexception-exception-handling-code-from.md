### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>ImageSourceConverter.ConvertFrom 之例外狀況處理程式碼中的 NullReferenceException

|   |   |
|---|---|
|詳細資料|<xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> 之例外狀況處理程式碼中的錯誤導致擲回不正確的 <xref:System.NullReferenceException?displayProperty=name>，而不是預期的例外狀況 (例如 <xref:System.IO.DirectoryNotFoundException?displayProperty=name>、<xref:System.IO.FileNotFoundException?displayProperty=name>)，這項變更會修正該錯誤，讓此方法現在會擲回正確的例外狀況。根據預設，以 .NET Framework 4.6.2 和以下版本為目標的所有應用程式仍會擲回 <xref:System.NullReferenceException?displayProperty=name> 來提供相容性，以 .NET Framework 4.7 和以上版本為目標的開發人員應該會看到正確的例外狀況。// 將空格取代為 'x' (如果適用的話)|
|建議|開發人員若想要在目標為 .NET Framework 4.7 時還原成取得 <xref:System.NullReferenceException?displayProperty=name>，可以在其應用程式的 App.config 檔案中新增/合併下列程式碼：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.7|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

