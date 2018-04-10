### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>具有 Regex.CompileToAssembly 4.0 和 4.5 之間的斷層編譯的組件

|   |   |
|---|---|
|詳細資料|如果組件編譯的規則運算式使用.NET Framework 4.5，但是目標.NET Framework 4 建立，請嘗試安裝.NET Framework 4 的系統上的組件，使用規則運算式的其中一個會擲回例外狀況。|
|建議|若要解決這個問題，您可以執行下列任何一項操作：<ul><li>建置包含規則運算式與.NET Framework 4 組件。</li><li>使用解譯的規則運算式。</li></ul>|
|範圍|次要|
|版本|4.5|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

