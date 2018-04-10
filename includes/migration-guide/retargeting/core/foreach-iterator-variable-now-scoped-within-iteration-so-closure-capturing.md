### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>Foreach 迭代器變數的領域現在設定反覆項目的，因此 closure 擷取語意不相同 （在 C# 5)

|   |   |
|---|---|
|詳細資料|開頭為 C# 5 (Visual Studio 2012)，<code>foreach</code>迭代器變數範圍內的反覆項目。 如果程式碼先前取決於未包含在變數，這可能會造成符號<code>foreach</code>的終止。 這項變更症狀就是建立在時間有委派的值時，而不是在叫用委派時的時間的值傳遞給委派的迭代器變數會被視為。|
|建議|在理想情況下，您應該更新程式碼，以確保此新的編譯器行為。 如果需要舊版語意，您可以將此迭代器變數取代成明確放在迴圈範圍外的不同變數。|
|範圍|主要|
|版本|4.5|
|類型|正在重定目標|

