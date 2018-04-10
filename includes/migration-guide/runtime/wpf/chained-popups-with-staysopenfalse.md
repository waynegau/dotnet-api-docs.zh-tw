### <a name="chained-popups-with-staysopenfalse"></a>鏈結快顯 staysopen = False

|   |   |
|---|---|
|詳細資料|快顯視窗 staysopen = False 應該關閉當您按一下快顯功能表外部。 當兩個或多個此類快顯會鏈結 （也就是其中一個包含另一個），發生許多問題，包括：<ul><li>開啟兩個層級，請按一下 P2 但 P1。  則不會發生。</li><li>開啟兩個層級中，按一下 外部 P1。  這兩個快顯視窗關閉。</li><li>開啟及關閉兩個層級。  然後嘗試再次開啟 P2。  則不會發生。</li><li>嘗試開啟三個層級。  您不能。  （沒有任何反應或關閉前兩個層級，請根據您在其中按一下。）這些情況下 （以及其他變數） 現在可正常運作。</li></ul>|
|範圍|Edge|
|版本|4.7.1|
|類型|執行階段|
|受影響的 API|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

