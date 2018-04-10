### <a name="ef-no-longer-throws-for-queryviews-with-specific-characteristics"></a>EF 不會再擲回 QueryViews 由特定特性

|   |   |
|---|---|
|詳細資料|Entity Framework 不再擲回<xref:System.StackOverflowException?displayProperty=name>例外狀況時應用程式執行查詢，以與 0..1 queryview 嘗試查詢中包含相關的實體的導覽屬性。 例如，藉由呼叫<code>.Include(e =&gt; e.RelatedNavProp)</code>。|
|建議|這項變更只會影響使用 QueryViews 1 的程式碼-0..1 關聯性，當執行查詢該呼叫。包含。 這項功能可提高可靠性，對於幾乎所有應用程式應該都是透明的。 不過，如果這項功能造成未預期的行為，您可以在應用程式組態檔的 <code>&lt;appSettings&gt;</code> 區段中加入下列項目，來停用這項功能：<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyUserSpecifiedViews&quot; value=&quot;false&quot; /&gt;&#13;&#10;</code></pre>|
|範圍|Edge|
|版本|4.5.2|
|類型|執行階段|

