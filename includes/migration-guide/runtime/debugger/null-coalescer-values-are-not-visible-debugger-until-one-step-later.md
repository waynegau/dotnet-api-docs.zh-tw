### <a name="null-coalescer-values-are-not-visible-in-debugger-until-one-step-later"></a>Null coalescer 值才會顯示偵錯工具中稍後的一個步驟

|   |   |
|---|---|
|詳細資料|.NET Framework 4.5 中的 bug 會透過設定 null 聯合作業不會顯示在偵錯工具指派作業會在 64 位元版本的 framework 上執行時執行之後，立即的值。|
|建議|逐步執行一個額外的時間，偵錯工具中，會導致本機/欄位的值正確更新。 此外，已在.NET Framework 4.6; 修正此問題升級至該版本的架構應可解決此問題。|
|範圍|Edge|
|版本|4.5|
|類型|執行階段|

