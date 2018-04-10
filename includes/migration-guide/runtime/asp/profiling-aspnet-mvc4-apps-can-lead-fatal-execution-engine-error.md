### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a>程式碼剖析 ASP.Net MVC4 應用程式可能會導致嚴重的執行引擎錯誤

|   |   |
|---|---|
|詳細資料|使用 NGEN /Profile 組件的程式碼剖析工具可能會當機分析的 ASP.NET MVC4 應用程式在啟動與 ' 嚴重執行引擎的例外狀況 '|
|建議|.NET Framework 4.5.2 中修正此問題。 或者，分析工具時，可能會藉由指定避免這個問題<code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code>其事件遮罩中。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|

