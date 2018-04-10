### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>WPF DataTemplate 項目現在都看得到 UIA

|   |   |
|---|---|
|詳細資料|先前，<xref:System.Windows.DataTemplate?displayProperty=name>元素已看不到使用者介面自動化。 從 4.5 開始，使用者介面自動化將會偵測這些項目。 這是在許多情況下，很有用，但可能會中斷依賴 UIA 樹狀目錄未包含測試<xref:System.Windows.DataTemplate?displayProperty=name>項目。|
|建議|UI 自動化測試此應用程式可能必須更新為帳戶現在包括 UIA 樹狀目錄的先前看不見<xref:System.Windows.DataTemplate?displayProperty=name>項目。 例如，預期某些項目彼此相鄰的測試，現在可能需要預期這些項目之間會出現先前不可見的 UIA 項目。 或者，依賴幾個 UIA 項目或其索引的測試，可能需要以新值更新。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

