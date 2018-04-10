反斜線 (\\) 是中的 mutex 名稱的保留的字元。 請勿使用反斜線 (\\) 以外的 mutex 名稱在終端機伺服器工作階段中使用 mutex 的注意事項中所指定。 否則，<xref:System.IO.DirectoryNotFoundException>可能會擲回，即使將 mutex 的名稱表示現有的檔案。
