### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET 現在會嘗試自動重新連接中斷的 SQL 連線

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.5.1 中的開始，.NET Framework 將嘗試自動重新連線中斷的 SQL 連線。 雖然這通常會讓應用程式更可靠，沒有應用程式必須知道的連線已中斷，讓它可以採取某些動作，在重新連線時的邊緣案例。|
|建議|如果基於相容性考量，您不需要這項功能，它可以設定來停用<xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name>連接字串的屬性 (或<xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) 設為 0。|
|範圍|Edge|
|版本|4.5.1|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|

