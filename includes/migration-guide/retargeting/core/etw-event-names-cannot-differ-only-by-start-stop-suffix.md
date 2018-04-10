### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>ETW 事件名稱不能只有不同 「 開始 」 或 「 停止 」 的尾碼

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.6 和 4.6.1 中，執行階段會擲回<xref:System.ArgumentException>當兩個事件追蹤的 Windows (ETW) 事件的名稱差異只在於&quot;啟動&quot;或&quot;停止&quot;尾碼 (做為一個事件時命名為<code>LogUser</code>和另一個名為<code>LogUserStart</code>)。 在此情況下，執行階段無法建構事件來源，因此無法發出任何記錄。|
|建議|若要避免這個例外狀況，請確定沒有兩個事件的名稱與只由不同&quot;啟動&quot;或&quot;停止&quot;後置詞。從.NET Framework 4.6.2; 移除這項需求執行階段可以釐清的差異只在於事件名稱&quot;啟動&quot;和&quot;停止&quot;後置詞。|
|範圍|Edge|
|版本|4.6|
|類型|正在重定目標|

