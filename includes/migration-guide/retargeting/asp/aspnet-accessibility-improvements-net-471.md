### <a name="aspnet-accessibility-improvements-in-net-471"></a>在.NET 4.7.1 ASP.NET 協助工具增強功能

|   |   |
|---|---|
|詳細資料|從.NET Framework 4.7.1 開始，ASP.NET 已經改良的 ASP.NET Web 控制項搭配 Visual Studio 中的協助工具技術，來更好的支援 ASP.NET 客戶的運作方式。  這些需求包括下列變更：<ul><li>若要在控制項中，實作遺漏 UI 協助工具模式變更，例如在詳細資料檢視精靈 的 新增欄位 對話方塊或 ListView 精靈的 設定 ListView 對話方塊。</li><li>若要改善在高對比模式中，顯示的變更，例如資料頁面巡覽區欄位編輯器。</li><li>變更以增進鍵盤瀏覽體驗控制項就像在 DataPager 控制項、 設定 ObjectContext 的對話方塊中或設定資料來源精靈的 設定資料選取項目 對話方塊的 編輯頁面巡覽區欄位精靈的 欄位 對話方塊。</li></ul>|
|建議|<strong>如何選擇加入或退出這些變更</strong>讓 Visual Studio 設計工具，可受益於這些變更，它必須在.NET Framework 4.7.1 上執行或更新版本。 Web 應用程式可以從這些變更的其中一種下列獲益：<ul><li>安裝 Visual Studio 2017 15.3 或更新版本中，依預設支援使用下列 AppContext 參數的新協助工具功能。</li><li>藉由新增退出舊版的協助工具行為<code>Switch.UseLegacyAccessibilityFeatures</code>AppContext 參數<code>&lt;runtime&gt;</code>區段內的 devenv.exe.config 檔案中，並將它設定為<code>false</code>，如下列範例所示。</li></ul><pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;...&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false&#39;  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;...;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;...&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>.NET Framework 4.7.1 為目標的應用程式或更新版本並想要保留舊版協助工具的行為也可以選擇使用舊版的協助工具功能的明確設為這個 AppContext 參數<code>true</code>。|
|範圍|次要|
|版本|4.7.1|
|類型|正在重定目標|

