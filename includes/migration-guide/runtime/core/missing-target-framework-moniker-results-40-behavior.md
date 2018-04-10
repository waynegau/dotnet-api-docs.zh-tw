### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>遺漏目標 Framework Moniker 產生 4.0 的行為

|   |   |
|---|---|
|詳細資料|應用程式不含<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>套用在組件層級將會自動使用.NET Framework 4.0 的語意 (quirks) 來執行。 為了確保高品質，我們建議所有二進位檔案，以明確屬性<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>表示原本建置時所使用的.NET framework 版本。 請注意，使用專案檔中的目標 framework moniker 會導致將自動套用的 MSBuild <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>。|
|建議|A<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>應該提供，方法是透過將屬性直接至組件，或藉由指定中的目標架構[專案檔案，或透過 Visual Studio 專案內容 GUI](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx)。|
|範圍|主要|
|版本|4.5|
|類型|執行階段|

