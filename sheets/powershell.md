# Powershell


## Tips
1. When developing scripts always run `pwsh.exe script/to/runMe.ps1` within a powershell cli (this is to counteract Gotcha#1)


## Gotchas
1. When developing powershell scripts, if the script loads a module. The session will not unload it once it's done, nor re-import it if you have made changes. 