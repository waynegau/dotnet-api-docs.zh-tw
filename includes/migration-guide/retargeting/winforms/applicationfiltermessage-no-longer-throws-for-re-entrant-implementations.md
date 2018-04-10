### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Application.FilterMessage 不再擲回之可重新進入的 IMessageFilter.PreFilterMessage 實作

|   |   |
|---|---|
|詳細資料|.NET Framework 4.6.1 之前，並呼叫<xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)>與<xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)>呼叫的目標<xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name>或<xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name>(同時也呼叫<xref:System.Windows.Forms.Application.DoEvents>) 會導致<xref:System.IndexOutOfRangeException?displayProperty=name>。從目標為.NET Framework 4.6.1 的應用程式，此例外狀況不會再擲回，並可重新進入 （如上所述） 可能會使用篩選。|
|建議|請注意，<xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)>將不再擲回的可重新進入<xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)>上面所述的行為。 這只會影響以.NET Framework 4.6.1.Apps 目標.NET Framework 4.6.1 即可退出這項變更 （或較舊的目標架構也可以選擇在應用程式） 為目標的應用程式使用[DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation)相容性參數。|
|範圍|Edge|
|版本|4.6.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

