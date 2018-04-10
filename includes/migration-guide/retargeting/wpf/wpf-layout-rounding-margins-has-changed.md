### <a name="wpf-layout-rounding-of-margins-has-changed"></a>邊界的進位的 WPF 版面配置已變更

|   |   |
|---|---|
|詳細資料|邊界的進位方式以及邊界內部的框線和背景皆有所變更。 此變更的結果：<ul><li>項目寬度或高度的增減最多不超過一個像素。</li><li>物件的位置的位最多不超過一個像素。</li><li>置中項目的垂直或水平位移最多不超過一個像素。</li></ul>預設只有以 .NET Framework 4.6 為目標的應用程式才會啟用此新版面配置。|
|建議|由於此修改會裁剪的右側或底端的高 Dpi 的 WPF 控制項，這種新行為可以選擇以舊版.NET Framework 為目標但在.NET Framework 4.6 上執行應用程式，將下列這一行加入<code>&lt;runtime&gt;</code> app.config 檔的區段： <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false&quot; /&gt;</code>.NET Framework 4.6 為目標，但想要使用先前的配置演算法所呈現的 WPF 控制項的應用程式可以這樣做將下列這一行加入<code>&lt;runtime&gt;</code>app.config 檔的區段：<code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=true&quot; /&gt;</code>.|
|範圍|次要|
|版本|4.6|
|類型|正在重定目標|

