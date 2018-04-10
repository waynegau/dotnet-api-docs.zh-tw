### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument 可能會顯示額外的程式行的文字

|   |   |
|---|---|
|詳細資料|在某些情況下，<xref:System.Windows.Documents.FlowDocument>項目相較於.NET Framework 4.0 上執行時，它的顯示方式，.NET Framework 4.5 上執行時，會顯示額外的程式行的文字。 沒有已知的情況下，變更會導致 illegibly，或完全無法顯示任何文字的但可能會導致出現的文字，從先前已省略<xref:System.Windows.Documents.FlowDocument>的檢視。|
|建議|在某些情況下，減少顯示項目的 PageHeight 屬性其中一個可以還原先前顯示的行數。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

