> [!NOTE]
> 從.NET Core 2.0 開始，您不需要執行[ `dotnet restore` ](~/docs/core/tools/dotnet-restore.md)因為它是以隱含方式執行的所有命令，例如`dotnet build`和`dotnet run`，需要進行還原。 它仍然是有效的命令，在某些情況下，執行明確的還原就有意義，例如[Visual Studio Team Services 中的連續整合組建](/vsts/build-release/apps/aspnet/build-aspnet-core)或建置系統是否需要明確地控制的時間進行還原。
>
> 此命令也支援`dotnet restore`時傳入的完整格式選項 (例如， `--source`)。 簡短形式選項，例如`-s`，不支援。