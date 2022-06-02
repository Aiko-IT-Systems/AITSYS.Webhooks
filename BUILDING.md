# Building AITSYS.Webhooks
These are detailed instructions on how to build the AITSYS.Webhooks library under various environmnets.

It is recommended you have prior experience with multi-target .NET Core/Standard projects, as well as the `dotnet` CLI utility, and MSBuild.

## Instructions
Once you install all the necessary prerequisites, you can proceed to building. These instructions assume you have already cloned the repository.

### Windows
Building on Windows is relatively easy. There's 2 ways to build the project:

#### Building through Visual Studio
Building through Visual Studio yields just binaries you can use in your projects.

1. Open the solution in Visual Studio.
2. Set the configuration to Release.
3. Select Build > Build Solution to build the project.
4. Select Build > Publish AITSYS.Webhooks to publish the binaries.

#### Building with the build script
Building this way outputs NuGet packages, and a documentation package. Ensure you have an internet connection available, as the script will install programs necessary to build the documentation.

1. Open PowerShell and navigate to the directory which you cloned AITSYS.Webhooks to.
2. Execute `.\s_oneclick-rebuild-all.ps1 -configuration Release` and wait for the script to finish execution.
3. Once it's done, the artifacts will be available in *aitsys-wh-artifacts* directory, next to the directory to which the repository is cloned.

### GNU/Linux
When all necessary prerequisites are installed, you can proceed to building. There are technically 2 ways to build the library, though both of them perform the same steps, they are just invoked slightly differently.

#### Through Visual Studio Code
1. Open Visual Studio Code and open the folder to which you cloned AITSYS.Webhooks as your workspace.
2. Select Build > Run Task...
3. Select `buildRelease` task and wait for it to finish.
4. The artifacts will be placed in *aitsys-wh-artifacts* directory, next to where the repository is cloned.

#### Through PowerShell
1. Open PowerShell (`pwsh`) and navigate to the directory which you cloned AITSYS.Webhooks to.
2. Execute `.\s_oneclick-rebuild-all.ps1 -configuration Release` and wait for the script to finish execution.
3. Once it's done, the artifacts will be available in *aitsys-wh-artifacts* directory, next to the directory to which the repository is cloned.
