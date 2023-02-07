# Windows


## Mapping Drives
1. Map a specific network folder to a drive.
    * `net use M: \\Michaelangelo\Yukon /persistent:Yes`
1. Map a local folder to a network drive folder, 
    * `subst R: C:\devel\rotor` <- this does not persistent after restarts. 
    * use [psubst](https://community.chocolatey.org/packages/psubst) to make it permenent
1. Install [chocoletery] (https://chocolatey.org/install)
