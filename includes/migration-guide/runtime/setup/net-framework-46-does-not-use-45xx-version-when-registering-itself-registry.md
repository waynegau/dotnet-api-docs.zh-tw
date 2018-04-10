### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>.NET Framework 4.6 中登錄註冊本身時不使用 4.5.x.x 版本

|   |   |
|---|---|
|詳細資料|如預期其中一個，版本機碼設定為登錄中 (在<code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) 的.NET Framework 4.6 開始使用 '4.6'，不 '4.5 的'。 應該更新相依於這些登錄機碼，知道在電腦上安裝的.NET Framework 版本的應用程式，以了解 4.6，新的可能版本，以及與先前 4.5.x 相容的其中一個版本。|
|建議|更新應用程式的.NET Framework 4.5 探查安裝尋找 4.5 的登錄機碼，也接受 4.6。|
|範圍|Edge|
|版本|4.6|
|類型|執行階段|

