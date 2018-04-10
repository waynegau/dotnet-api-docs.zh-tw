### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>在單一監視器之外擴充 WPF 視窗呈現而不裁剪

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.6 執行 Windows 8 和更新版本中，會在而不裁剪呈現整個視窗時它會擴充在多重監視器案例中的單一顯示之外。 這是不同於舊版.NET Framework 會裁剪 WPF 視窗超過單一顯示擴充。|
|建議|這項行為 （不論裁剪或不是） 可以明確設定使用<code>&lt;EnableMultiMonitorDisplayClipping&gt;</code>中的項目<code>&lt;appSettings&gt;</code>應用程式的組態檔中，或藉由設定<code>EnableMultiMonitorDisplayClipping</code>屬性在應用程式啟動。|
|範圍|次要|
|版本|4.6|
|類型|執行階段|

