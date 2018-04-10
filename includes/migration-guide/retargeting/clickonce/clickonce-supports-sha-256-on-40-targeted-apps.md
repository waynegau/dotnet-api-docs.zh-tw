### <a name="clickonce-supports-sha-256-on-40-targeted-apps"></a>ClickOnce 支援 sha-256 4.0 為目標的應用程式

|   |   |
|---|---|
|詳細資料|先前，與憑證使用 sha-256 簽署的 ClickOnce 應用程式需要.NET 4.5 或更新版本為存在，即使應用程式目標 4.0。 現在，4.0 為目標的 ClickOnce 應用程式可以在執行 4.0 中，即使使用 SHA 256 進行簽署。|
|建議|這項變更移除了該相依性，並允許使用 sha-256 憑證用來簽署 ClickOnce 應用程式，以.NET Framework 4 和舊版為目標。|
|範圍|次要|
|版本|4.6|
|類型|正在重定目標|

