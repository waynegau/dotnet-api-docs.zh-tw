### <a name="wpf-spell-checking-fails-in-unexpected-ways"></a>WPF 拼字檢查會失敗，非預期的方式

|   |   |
|---|---|
|詳細資料|這包括 WPF 拼字檢查工具的問題數目：<ul><li>WPF 拼字檢查程式有時會擲回 <xref:System.Runtime.InteropServices.COMException?displayProperty=name></li><li>WPF 拼字檢查會失敗並<xref:System.UnauthorizedAccessException>時使用 [以不同使用者身分執行] 啟動應用程式</li><li>WPF 拼字檢查工具不正確地識別複合 'Hausnummer' 德文的文字中的拼字錯誤。</li></ul>|
|建議|問題 #1-此問題已在.NET Framework 4.6.2 中修正問題 #2-WPF 拼字檢查工具已不再支援使用 [以不同使用者身分執行] 啟動應用程式時。 從.NET Framework 4.6.2，以這種方式啟動應用程式將不再會損毀意外-改用拼字檢查將會以無訊息方式停用。 問題 #3-此問題已在.NET Framework 4.6.2 中修正。|
|範圍|Edge|
|版本|4.6.1|
|類型|執行階段|

