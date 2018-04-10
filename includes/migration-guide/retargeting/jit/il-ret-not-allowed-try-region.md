### <a name="il-ret-not-allowed-in-a-try-region"></a>IL ret 再試一次區域中不允許

|   |   |
|---|---|
|詳細資料|不同於 JIT64 中 just-in-time 編譯器，RyuJIT （用於.NET 4.6） 不允許 IL ret 再試一次區域中的指示。 傳回從 try 區域不允許在 ECMA 335 規格中，並沒有已知的 managed 的編譯器產生這類 IL。 不過，如果這類 IL 是由反映發出所產生，則 JIT64 編譯器將會執行這類 IL。|
|建議|如果應用程式產生包含 ret opcode，再試一次區域中的 IL，應用程式可能會以目標.NET 4.5，即可使用舊的 JIT，以避免這個分行符號。 或者，傳回之後再試一次區域可能會更新產生的 IL。|
|範圍|Edge|
|版本|4.6|
|類型|正在重定目標|

