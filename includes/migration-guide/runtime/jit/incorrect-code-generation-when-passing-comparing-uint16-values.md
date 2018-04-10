### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>不正確的程式碼產生時傳遞和比較 UInt16 值

|   |   |
|---|---|
|詳細資料|由於.NET Framework 4.7 中導入的變更，在某些情況下產生 JIT 編譯器的不正確地執行於.NET Framework 4.7 應用程式的程式碼比較兩個<code>T:System.UInt16</code>值。 如需詳細資訊，請參閱[問題 #11508： 無訊息錯誤 codegen 時傳遞和比較 ushort args](https://github.com/dotnet/coreclr/issues/11508) GitHub.com 上。|
|建議|如果您遇到問題，在 16 位元不帶正負號的值，在.NET Framework 4.7 比較中，升級至.NET Framework 4.7.1。|
|範圍|Edge|
|版本|4.7|
|類型|執行階段|

