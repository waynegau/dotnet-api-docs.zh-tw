### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>SqlBulkCopy 使用目的地資料行編碼字串

|   |   |
|---|---|
|詳細資料|將資料插入資料行時，<xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> 會使用目的地資料行的編碼方式，而不是 <code>VARCHAR</code> 和 <code>CHAR</code> 類型的預設編碼方式。 這項變更可排除當目的地資料行未使用預設編碼方式時，使用預設編碼方式可能造成的資料損毀。 在罕見的情況下，現有的應用程式可能會擲回 SqlException 例外狀況，如果變更編碼方式後產生的太大而無法放入目的地資料行的資料。|
|建議|預期<xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name>不再損毀資料，因為編碼方式的差異。 如果正在複製接近目的地資料行的大小限制的字串，它可能必須是預先編碼 （要複製資料來檢查資料將符合的目的地資料行中） 或 catch <xref:System.Data.SqlClient.SqlException?displayProperty=name>s。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

