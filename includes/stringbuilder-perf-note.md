使用以字元為基礎的索引與<xref:System.Text.StringBuilder.Chars%2A>屬性可以是很慢，在下列情況下：

- <xref:System.Text.StringBuilder>很大的執行個體 （例如，它包含數個數以萬計的字元）。
- <xref:System.Text.StringBuilder>是 「 大量 」。 也就是說，例如重複方法的呼叫<xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType>自動展開物件的<xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType>屬性和配置的記憶體給它的新區塊。

因為每個字元的存取會逐步引導整個連結的清單來尋找正確的緩衝區索引的區塊會嚴重影響效能。

> [!NOTE]
>  即使對於大型 「 大量 」<xref:System.Text.StringBuilder>物件、 使用<xref:System.Text.StringBuilder.Chars%2A>索引為基礎的存取，其中一個或少數幾個字元的屬性些許的效能影響; 一般來說，這是**0 （n)**作業。 反覆查看中的字元時，就會發生顯著的效能影響<xref:System.Text.StringBuilder>物件，它是**O(n^2)**作業。 

如果使用以字元為基礎的索引時，會遇到效能問題<xref:System.Text.StringBuilder>物件，您可以使用任何下列因應措施：

- 轉換<xref:System.Text.StringBuilder>執行個體<xref:System.String>藉由呼叫<xref:System.Text.StringBuilder.ToString%2A>方法，然後存取字串中的字元。

- 將現有的內容複製<xref:System.Text.StringBuilder>物件至新預留的大小<xref:System.Text.StringBuilder>物件。 效能改善，因為新<xref:System.Text.StringBuilder>物件不是大量。 例如: 

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- 設定的初始容量<xref:System.Text.StringBuilder>物件的值，藉由呼叫是大約等於其大小上限的預期<xref:System.Text.StringBuilder.%23ctor(System.Int32)>建構函式。 請注意這會配置記憶體，即使整個區塊<xref:System.Text.StringBuilder>很少達到最大容量。
