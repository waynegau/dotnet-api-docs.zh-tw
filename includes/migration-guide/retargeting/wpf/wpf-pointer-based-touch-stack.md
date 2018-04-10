### <a name="wpf-pointer-based-touch-stack"></a>WPF 指標為基礎的觸控堆疊

|   |   |
|---|---|
|詳細資料|這項變更將能夠啟用選擇性的 WM_POINTER 基礎 WPF 觸控/手寫筆堆疊。  請勿明確地啟用此的開發人員應該會看到 WPF 觸控/手寫筆行為沒有變更。已知問題與選擇性的 WM_POINTER 目前型觸控/手寫筆堆疊：<ul><li>不支援即時筆跡。</li><li>同時筆跡 StylusPlugins 也還能運作，這可能會導致效能不佳 UI 執行緒上進行處理。</li><li>因為升級觸控/手寫筆事件從滑鼠事件已變更的行為變更</li><li>操作可能會有不同的行為</li><li>拖放不會顯示為具備觸控輸入適當的回應</li><li>這不會影響手寫筆輸入</li><li>拖放可以不再起始觸控/手寫筆事件</li><li>這可能會使應用程式停止回應到偵測到滑鼠輸入為止。</li><li>開發人員應改為從滑鼠事件起始拖放動作。</li></ul>|
|建議|開發人員想要啟用此堆疊可以加入/合併至其應用程式的 App.config 檔下：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Input.Stylus.EnablePointerSupport=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>移除此或將值設定為 false 將會關閉這個選擇性的堆疊。請注意，此堆疊是使用只在 Windows 10 建立者更新與更新版本。|
|範圍|Edge|
|版本|4.7|
|類型|正在重定目標|

