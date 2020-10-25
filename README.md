# [Any] Command Dumper
**Current Version: 1.1.0**  




## Description:

 This plugin will create a file (plaintext or .csv) with all SM-created commands, along with their descriptions and required admin flags.  
 For more info, see  **Notes**.  

**Example CSV Output:**  
(Sorted by command name)   
[![](https://forums.alliedmods.net/image-proxy/fcf7979c01f0d443da5829301d372ecad12be243/687474703a2f2f636f6e74656e742e73637265656e636173742e636f6d2f75736572732f44617274684e696e6a612f666f6c646572732f4a696e672f6d656469612f63343762396237332d303531372d346135652d393066302d3062313166613935626264362f4353565f44656d6f312e706e67)](http://content.screencast.com/users/DarthNinja/folders/Jing/media/c47b9b73-0517-4a5e-90f0-0b11fa95bbd6/CSV_Demo1.png)

## Commands:

-   ****sm_dumpcommands****
    -   Dumps all commands to a file.


## Cvars:

-   **sm_commanddump_version**
    -   Plugin Version
-   **sm_commanddump_use_csv**
    -   0 = The plugin will output to a .txt file (default).
    -   1 = The plugin will output to a .csv file. Useful for importing into excel/google docs/etc so you can sort commands by flag, etc.

## Install Instructions:

1.  Place  **CommandDump****.smx**  into your addons/sourcemod/plugins/ folder.


## Notes:

-   The plugin will tell you the location of the output file when you run the command.
-   The plugin is only able to detect adminflags that are registered when the command is registered.  
    Plugins that use CheckCommandAccess or equivalent in the callback will be reported as "No flag registered".
-   The plugin will report flags as they appear on the server. A slay command that is overridden to ban will be detected as "ADMFLAG_BAN".


## Version History:  

-   **V1.0.0**
    -   Initial Release
-   **V1.0.1**
    -   No longer loads common.phrases as doing so is not required.
-   **V1.1.0**
    -   Now handles commands that use multiple flags properly.
