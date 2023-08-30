# IDAExecFunctionsImporter

## This is an IDA-Plugin to import names from a file into the database.

### This plugin can be used with .idmap files generated by [Dumper-7](https://github.com/Encryqed/Dumper-7/).
-----
Currently imported:
- Virtual Function Table names: eg. UClass_VFT
- UFunction::ExecFunction names: eg. APlayerController::execCanRestartPlayer

-----

### The expected format is:
```c++
struct Identifier
{
    uint32 Offset; // Relative to Imagebase
    uint16 NameLength;
    const char Name[NameLength]; // Not NULL-terminated
};
```
-----
Exec-Functions             |  VirtualFunctionTables
:-------------------------:|:-------------------------:
![image](https://github.com/Fischsalat/IDAExecFunctionsImporter/assets/64608145/15b7c443-2742-40f5-8071-4238448b6269)  |  ![image](https://github.com/Fischsalat/IDAExecFunctionsImporter/assets/64608145/bfc1ab5b-c2df-4123-ac9d-208f77c2cc12)





