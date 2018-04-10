### <a name="wpf-printing-stack-update"></a>WPF 列印堆疊更新

|   |   |
|---|---|
|詳細資料|WPF 的列印應用程式開發介面使用<xref:System.Printing.PrintQueue?displayProperty=name>現在呼叫視窗列印文件封裝 API 現在已被取代的 XPS 列印 API 改用。 變更與服務性記住;使用者和開發人員都不應該會看到行為或應用程式開發介面使用方式中的任何變更。 在 Windows 10 建立者更新中執行時，預設會啟用新的列印堆疊。 舊的列印堆疊仍會繼續只要如常運作，在舊版本的 Windows 中。|
|建議|若要在 Windows 10 建立者更新使用舊的堆疊， <code>UseXpsOMPrinting</code> REG_DWORD 值<code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code>登錄機碼<code>1</code>。|
|範圍|Edge|
|版本|4.7|
|類型|執行階段|

