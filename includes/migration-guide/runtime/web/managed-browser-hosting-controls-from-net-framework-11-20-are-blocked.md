### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>封鎖受管理瀏覽器裝載控制項上的，從.NET Framework 1.1 和 2.0 版

|   |   |
|---|---|
|詳細資料|Internet Explorer 中已封鎖裝載這些控制項。|
|建議|Internet Explorer 將無法啟動使用 Managed 瀏覽器裝載控制項的應用程式。 可以還原舊有行為的登錄子機碼值<code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code>至<code>1</code>適用於 x86 系統和 x64 上的 32 位元處理序系統，以及設定<code>EnableIEHosting</code>的登錄子機碼值<code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>至<code>1</code>x64 上的 64 位元處理序的系統。|
|範圍|次要|
|版本|4.5|
|類型|執行階段|

