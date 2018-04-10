### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>若要還原從不同 4.5 SQL 產生更簡單 4.0 版的 SQL 產生選擇加入的中斷

|   |   |
|---|---|
|詳細資料|產生聯結陳述式，而且包含呼叫的查詢限制的作業，但未先使用 OrderBy 現在會產生更簡單的 SQL。 升級至.NET Framework 4.5 之後，這些查詢會產生比舊版更複雜的 SQL。|
|建議|預設已停用這項功能。 如果 Entity Framework 產生額外的聯結陳述式而造成效能降低，您可以藉由新增下列項目，以啟用此功能<code>&lt;appSettings&gt;</code>應用程式組態檔 (app.config) 的區段：<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|範圍|透明|
|版本|4.5.2|
|類型|執行階段|

