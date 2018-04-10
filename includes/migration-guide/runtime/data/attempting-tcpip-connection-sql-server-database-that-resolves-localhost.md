### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>嘗試解析成 SQL Server 資料庫的 TCP/IP 連接`localhost`失敗

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.6 和 4.6.1，嘗試解析成 SQL Server 資料庫的 TCP/IP 連接<code>localhost</code>失敗，發生錯誤，&quot;建立 SQL Server 的連接時發生網路相關或執行個體特定錯誤。 找不到或無法存取伺服器。 確認執行個名稱是否正確，以及 SQL Server 是否設定為允許遠端連線 (提供者： SQL 網路介面，錯誤： 26-尋找指定時發生錯誤伺服器/執行個體)&quot;|
|建議|在解決這個問題，並在.NET Framework 4.6.2 還原先前的行為。 若要連接到 SQL Server databsae 解析成<code>localhost</code>、 升級至.NET Framework 4.6.2。|
|範圍|次要|
|版本|4.6|
|類型|執行階段|

