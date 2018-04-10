### <a name="persian-calendar-now-uses-the-hijri-solar-algorithm"></a>波斯曆現在會使用回教陽曆演算法

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.6 開始<xref:System.Globalization.PersianCalendar?displayProperty=name>類別會使用回教陽曆演算法。 轉換日期之間<xref:System.Globalization.PersianCalendar?displayProperty=name>，而其他行事曆可能產生稍微不同的結果以開頭的.NET Framework 4.6 的日期早於 1800年或更晚 2023 （西曆）。此外，<xref:System.Globalization.PersianCalendar.MinSupportedDateTime>現在<code>March 22, 0622 instead of March 21, 0622</code>。|
|建議|請注意，在 .NET 4.6 中使用 PersianCalendar 時，某些較早或較晚的日期可能會稍微不同。 此外，在不同 .NET Framework 版本上執行的處理序之間序列化日期，不會將日期儲存為 PersianCalendar 日期字串 (因為這些值可能不同)。|
|範圍|次要|
|版本|4.6|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Globalization.PersianCalendar?displayProperty=nameWithType></li></ul>|

