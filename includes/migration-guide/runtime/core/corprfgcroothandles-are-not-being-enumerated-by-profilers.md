### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>COR_PRF_GC_ROOT_HANDLEs 不在列舉的程式碼剖析工具

|   |   |
|---|---|
|詳細資料|在.NET Framework v4.5.1，程式碼剖析 API<code>RootReferences2()</code>錯誤永遠不會傳回<code>COR_PRF_GC_ROOT_HANDLE</code>(它們做為傳回<code>COR_PRF_GC_ROOT_OTHER</code>改為)。 從.NET Framework 4.6 開始，已修正此問題。|
|建議|.NET Framework 4.6 中已修正此問題，而且定址方式可透過升級至.NET Framework 的版本。|
|範圍|次要|
|版本|4.5.1|
|類型|執行階段|

