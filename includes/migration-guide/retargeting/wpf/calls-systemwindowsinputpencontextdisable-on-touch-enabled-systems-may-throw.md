### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>呼叫 System.Windows.Input.PenContext.Disable 具有觸控功能的系統上可能會擲回 ArgumentException

|   |   |
|---|---|
|詳細資料|在某些情況下，呼叫內部<strong>System.Windows.Intput.PenContext.Disable</strong>具有觸控功能的系統上的方法可能會擲回未處理<code>T:System.ArgumentException</code>由於重新進入。|
|建議|在.NET Framework 4.7，已經解決這個問題。 若要避免這個例外狀況，升級至.NET Framework 4.7 為開頭的.NET framework 版本。|
|範圍|Edge|
|版本|4.6.1|
|類型|正在重定目標|

