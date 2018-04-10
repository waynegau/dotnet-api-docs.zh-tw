### <a name="listsort-algorithm-changed"></a>List.Sort 演算法已變更

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.5、<xref:System.Collections.Generic.List%601?displayProperty=name>的排序演算法已變更 （要內省式排序，而不是快速排序）。 <xref:System.Collections.Generic.List%601?displayProperty=name>排序從未穩定，但這項變更可能會導致不同的案例來排序不穩定的方式。 這只是表示對等項目可能會以不同的應用程式開發介面的後續呼叫中的順序排序。|
|建議|因為舊的排序演算法也不穩定 （即使在不同的方式），應一律以特定順序排序的對等項目所依賴的任何程式碼。 如果執行個體的程式碼，而定，而且正在幸運與舊的行為，該程式碼應該更新為使用決定性的方式會比較子來排序所需的順序中的項目。|
|範圍|透明|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

