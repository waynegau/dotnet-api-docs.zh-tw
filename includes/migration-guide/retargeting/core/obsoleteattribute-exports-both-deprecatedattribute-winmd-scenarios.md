### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute 將匯出為 ObsoleteAttribute 和 DeprecatedAttribute WinMD 案例中

|   |   |
|---|---|
|詳細資料|當您建立 Windows 中繼資料 （.winmd 檔案），<xref:System.ObsoleteAttribute?displayProperty=name>屬性匯出為<xref:System.ObsoleteAttribute?displayProperty=name>和[Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute)。|
|建議|重新編譯現有來源使用的程式碼<xref:System.ObsoleteAttribute?displayProperty=name>屬性可能會產生警告時使用該程式碼從 C + + /CX 或 JavaScript.We 不建議您同時套用<xref:System.ObsoleteAttribute?displayProperty=name>和[Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) managed 組件; 中的程式碼可能會導致建置警告。|
|範圍|Edge|
|版本|4.5.1|
|類型|正在重定目標|

