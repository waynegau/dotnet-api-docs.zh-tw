### <a name="marshalsizeof-and-marshalptrtostructure-overloads-break-dynamic-code"></a>Marshal.SizeOf 以及 Marshal.PtrToStructure 多載中斷動態程式碼

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.5.1，動態地繫結至方法<xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601>， <xref:System.Runtime.InteropServices.Marshal.SizeOf%60%601(%60%600)>， <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Object)>， <xref:System.Runtime.InteropServices.Marshal.PtrToStructure(System.IntPtr,System.Type)>， <xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr)>，或<xref:System.Runtime.InteropServices.Marshal.PtrToStructure%60%601(System.IntPtr,%60%600)>、 （透過 Windows PowerShell、 IronPython 或 C# 動態關鍵字，例如）可能會導致<code>MethodInvocationExceptions</code>因為已加入新的多載這些方法可能是指令碼引擎以模稜兩可。|
|建議|更新指令碼以清楚指出應該使用哪一個多載。 一般而言，將方法的型別參數明確轉換成 <xref:System.Type>，即可完成此作業。 如需如何解決問題的詳細資訊和範例，請參閱[這個連結](https://support.microsoft.com/kb/2909958/)。|
|範圍|次要|
|版本|4.5.1|
|類型|執行階段|

