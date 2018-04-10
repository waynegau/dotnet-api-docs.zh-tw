### <a name="unicode-standard-version-80-categories-now-supported"></a>現在支援 Unicode 標準 8.0 版類別

|   |   |
|---|---|
|詳細資料|在.NET Framework 4.6.2 framework 中的 Unicode 資料已升級從 Unicode 標準 6.3 版至 8.0 版。  當.NET Framework 4.6.2 中的 Unicode 字元分類要求時，某些結果可能不符合舊版的.NET Framework 中的結果。  這項變更通常會影響 Cherokee 音節和新的 Ta1 Lue 母音符號和音調標記。|
|建議|檢閱程式碼，並移除/變更邏輯取決於硬式編碼的 Unicode 字元分類。|
|範圍|次要|
|版本|4.6.2|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

