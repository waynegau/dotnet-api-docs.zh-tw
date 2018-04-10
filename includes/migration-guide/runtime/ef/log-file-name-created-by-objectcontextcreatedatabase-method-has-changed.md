### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>ObjectContext.CreateDatabase 方法所建立的記錄檔名稱已變更為符合 SQL Server 規格

|   |   |
|---|---|
|詳細資料|當<xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name>方法呼叫是直接或透過使用 Code First 搭配 SqlClient 提供者和連接字串中的 AttachDBFilename 值，它會建立名為而不是 filename.ldf filename_log.ldf （其中 filename 是名稱的記錄檔AttachDBFilename 值所指定的檔案）。 這項變更可透過提供依據 SQL Server 規格命名的記錄檔改善偵錯功能。|
|建議|如果記錄檔名稱對應用程式很重要，則應更新應用程式以採用標準 _log.ldf 檔案名稱格式。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

