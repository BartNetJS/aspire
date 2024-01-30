dotnet new aspire-starter --output AspireSample                  
The template ".NET Aspire Starter Application" was created successfully.
This template contains technologies from parties other than Microsoft, see https://aka.ms/aspire/1.0-third-party-notices for details.

Processing post-creation actions...
Restoring C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.sln:
  Determining projects to restore...
  Restored C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.Web\AspireSample.Web.csproj (in 1,41 sec).
  Restored C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.ApiService\AspireSample.ApiService.csproj (in 1,41 sec).
  Restored C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.AppHost\AspireSample.AppHost.csproj (in 1,41 sec).
  Restored C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.ServiceDefaults\AspireSample.ServiceDefaults.csproj (in 1,41 sec).
Restore succeeded.
Restoring C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.AppHost\AspireSample.AppHost.csproj:
  Determining projects to restore...
  All projects are up-to-date for restore.
Restore succeeded.
Restoring C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.ServiceDefaults\AspireSample.ServiceDefaults.csproj:
  Determining projects to restore...
  All projects are up-to-date for restore.
Restore succeeded.
Restoring C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.ApiService\AspireSample.ApiService.csproj:
  Determining projects to restore...
  All projects are up-to-date for restore.
Restore succeeded.
Restoring C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.Web\AspireSample.Web.csproj:
  Determining projects to restore...
  All projects are up-to-date for restore.
Restore succeeded.


C:\Users\[user name]\sources\playground\aspire
>azd infra synth --debug
2024/01/30 11:16:36 main.go:54: azd version: 1.5.1 (commit 3856d1e98281683b8d112e222c0a7c7b3e148e96)
2024/01/30 11:16:36 main.go:208: using cached latest version: 1.5.1 (expires on: 2024-01-30T10:19:12Z)
Error: no project exists; to create a new project, run `azd init`
C:\Users\[user name]\sources\playground\aspire
>azd init

Initializing an app to run on Azure (azd init)

? How do you want to initialize your app? Use code in the current directory

  (✓) Done: Scanning app code in current directory

Ignoring other projects present but not referenced by app host: AspireSample\AspireSample.ApiService and AspireSample\AspireSample.Web

Detected services:

  .NET (Aspire)
  Detected in: C:\Users\[user name]\sources\playground\aspire\AspireSample\AspireSample.AppHost\AspireSample.AppHost.csproj

azd will generate the files necessary to host your app on Azure using Azure Container Apps.

? Select an option Confirm and continue initializing my app
By default, a service can only be reached from inside the Azure Container Apps environment it is running in. Selecting a service here will also allow it to be reached from the Internet.
? Select which services to expose to the Internet webfrontend
? Enter a new environment name: [? for help] aspire-test

? Enter a new environment name: aspire-test

Generating files to run your app on Azure:

  (✓) Done: Generating ./azure.yaml
  (✓) Done: Generating ./next-steps.md

SUCCESS: Your app is ready for the cloud!
You can provision and deploy your app to Azure by running the azd up command in this directory. For more information on configuring your app, see ./next-steps.md
C:\Users\[user name]\sources\playground\aspire
>azd infra synth --debug
2024/01/30 11:17:41 main.go:54: azd version: 1.5.1 (commit 3856d1e98281683b8d112e222c0a7c7b3e148e96)
2024/01/30 11:17:41 main.go:208: using cached latest version: 1.5.1 (expires on: 2024-01-30T10:19:12Z)
2024/01/30 11:17:41 project.go:113: Reading project from file 'C:\Users\[user name]\sources\playground\aspire\azure.yaml'
2024/01/30 11:17:41 cobra_builder.go:141: Resolved action 'azd-infra-synth-action'
2024/01/30 11:17:41 middleware.go:124: running middleware 'debug'
2024/01/30 11:17:41 middleware.go:124: running middleware 'experimentation'
2024/01/30 11:17:41 experimentation.go:42: assignment context: 0g5ad841:76970;
2024/01/30 11:17:41 middleware.go:124: running middleware 'telemetry'
2024/01/30 11:17:41 telemetry.go:50: TraceID: cf6a3a3f73d8757c914dbc1370b0875f

WARNING: Feature 'infraSynth' is in alpha stage.
To learn more about alpha features and their support, visit https://aka.ms/azd-feature-stages.

  |====   | Analyzing Aspire Application (this might take a moment...)2024/01/30 11:17:44 command_runner.go:307: Run exec: 'dotnet run --project AspireSample.AppHost.csproj --publisher manifest --output-path C:\Users\BARTVA~1\AppData\Local\Temp\azd-provision3019814183\apphost-manifest.json' , exit code: 0
-------------------------------------stdout-------------------------------------------
Building...
info: Aspire.Hosting.Publishing.ManifestPublisher[0]
      Published manifest to: C:\Users\[user name]\AppData\Local\Temp\azd-provision3019814183\apphost-manifest.json
2024/01/30 11:17:44 infra_synth.go:164: infrastructure synth, checking for duplicates. source: C:\Users\BARTVA~1\AppData\Local\Temp\infra-synth4123246365 target: C:\Users\[user name]\sources\playground\aspire
C:\Users\[user name]\sources\playground\aspire
>