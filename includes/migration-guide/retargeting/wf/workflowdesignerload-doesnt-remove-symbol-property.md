### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load 並不會移除符號屬性

|   |   |
|---|---|
|詳細資料|當目標為.NET Framework 4.5，在工作流程設計工具，以及載入與 3.5 的重新裝載工作流程時<xref:System.Activities.Presentation.WorkflowDesigner.Load>方法，<xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name>儲存工作流程時擲回。|
|建議|.NET Framework 4.5 中的工作流程設計工具中，為目標，讓它可以克服藉由設定時，這個 bug 只資訊清單<code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code>至 4.0.NET Framework.Alternatively，問題可能避免使用<xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)>方法來載入工作流程，而不是<xref:System.Activities.Presentation.WorkflowDesigner.Load>。|
|範圍|主要|
|版本|4.5|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

