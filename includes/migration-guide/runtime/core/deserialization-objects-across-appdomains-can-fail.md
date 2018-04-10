### <a name="deserialization-of-objects-across-appdomains-can-fail"></a>無法還原序列化的物件跨越 appdomain

|   |   |
|---|---|
|詳細資料|在某些情況下，當應用程式使用具有不同應用程式基底的兩個或多個應用程式網域時，嘗試在邏輯呼叫內容中還原序列化跨應用程式網域的物件會擲回例外狀況。|
|建議|請參閱[風險降低： 還原序列化跨應用程式網域的物件](~/docs/framework/migration-guide/mitigation-deserialization-of-objects-across-app-domains.md)|
|範圍|Edge|
|版本|4.5.1|
|類型|執行階段|

