### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>HtmlTextWriter 不會呈現`<br/>`項目正確

|   |   |
|---|---|
|詳細資料|從 .NET Framework 4.6 開始，使用 <code>&lt;BR /&gt;</code> 項目呼叫 <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> 和 <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> 將會正確地只插入一個 <code>&lt;BR /&gt;</code> (而不是兩個)|
|建議|如果應用程式需要額外的 <code>&lt;BR /&gt;</code> 標籤，則應該再次呼叫 <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)>。 請注意，這種行為的變更只會影響應用程式的目標.NET Framework 4.6 或更新版本，讓另一個選項是以舊版.NET Framework 目標以取得舊的行為。|
|範圍|Edge|
|版本|4.6|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

