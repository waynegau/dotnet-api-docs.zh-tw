### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>工作流程 SQL 持續性加入叢集主索引鍵，且允許某些資料行中的 null 值

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.7 開始，SqlWorkflowInstanceStoreSchema.sql 指令碼所建立的 SQL 工作流程執行個體存放區 (SWIS) 的資料表使用叢集的主索引鍵。 因為這個緣故，不支援識別<code>null</code>值。 SWIS 作業不會受到這項變更。 若要支援 SQL Server 異動複寫進行的更新。|
|建議|SQL 檔案 SqlWorkflowInstanceStoreSchemaUpgrade.sql 必須套用到現有安裝，才能發生這項變更。 新的資料庫安裝將會自動有變更。|
|範圍|Edge|
|版本|4.7|
|類型|執行階段|

