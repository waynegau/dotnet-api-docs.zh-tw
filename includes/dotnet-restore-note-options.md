> [!NOTE]
> <span data-ttu-id="71377-101">從.NET Core 2.0 開始，您不需要執行[ `dotnet restore` ](~/docs/core/tools/dotnet-restore.md)因為它是以隱含方式執行的所有命令，例如`dotnet build`和`dotnet run`，需要進行還原。</span><span class="sxs-lookup"><span data-stu-id="71377-101">Starting with .NET Core 2.0, you don't have to run [`dotnet restore`](~/docs/core/tools/dotnet-restore.md) because it's run implicitly by all commands, such as `dotnet build` and `dotnet run`, that require a restore to occur.</span></span> <span data-ttu-id="71377-102">它仍然是有效的命令，在某些情況下，執行明確的還原就有意義，例如[Visual Studio Team Services 中的連續整合組建](/vsts/build-release/apps/aspnet/build-aspnet-core)或建置系統是否需要明確地控制的時間進行還原。</span><span class="sxs-lookup"><span data-stu-id="71377-102">It's still a valid command in certain scenarios where doing an explicit restore makes sense, such as [continuous integration builds in Visual Studio Team Services](/vsts/build-release/apps/aspnet/build-aspnet-core) or in build systems that need to explicitly control the time at which the restore occurs.</span></span>
>
> <span data-ttu-id="71377-103">此命令也支援`dotnet restore`時傳入的完整格式選項 (例如， `--source`)。</span><span class="sxs-lookup"><span data-stu-id="71377-103">This command also supports the `dotnet restore` options when passed in the long form (for example, `--source`).</span></span> <span data-ttu-id="71377-104">簡短形式選項，例如`-s`，不支援。</span><span class="sxs-lookup"><span data-stu-id="71377-104">Short form options, such as `-s`, are not supported.</span></span>