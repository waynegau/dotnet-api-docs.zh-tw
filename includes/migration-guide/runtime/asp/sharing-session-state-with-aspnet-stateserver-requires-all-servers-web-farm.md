### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>共用工作階段狀態與 Asp.Net StateServer 需要 web 伺服器陣列使用相同的.NET Framework 版本中的所有伺服器

|   |   |
|---|---|
|詳細資料|啟用時<xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name>工作階段狀態時，所有指定之 web 伺服陣列中的伺服器必須使用相同版本的.NET Framework 中狀態的順序正確共用。|
|建議|請務必將同時共用狀態的 web 伺服器上的.NET Framework 版本升級。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

