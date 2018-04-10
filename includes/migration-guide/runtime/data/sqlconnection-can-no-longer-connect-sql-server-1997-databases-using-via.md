### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection 無法再連接到 SQL Server 1997 或使用 VIA 配接器的資料庫

|   |   |
|---|---|
|詳細資料|使用 SQL Server 資料庫的連接[虛擬介面卡 (VIA) 通訊協定](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx)不再支援。 用來連接到 SQL Server 資料庫的通訊協定中會顯示連接字串。 VIA 連接將會包含透過：&lt;servername&gt;。 如果此應用程式連接到 SQL 透過 VIA 以外的通訊協定 (tcp： 或 np： 例如)，則會不發生任何重大變更。此外，不再支援 SQL Server 7 (1997) 的連線。|
|建議|VIA 通訊協定已被取代，因此請使用替代的通訊協定來連接至 SQL 資料庫。 使用的最常見的通訊協定是 TCP/IP。 您可以找到啟用 TCP/IP 通訊協定的指示[這裡](https://msdn.microsoft.com/library/bb909712.aspx)。 如果從內部網路中只能存取資料庫，共用的管道通訊協定可能提供較佳的效能，如果網路太慢。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

