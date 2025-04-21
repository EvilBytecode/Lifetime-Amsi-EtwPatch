# Lifetime-Amsi-EtwPatch
<a href="https://t.me/pulzetools"><img src="https://img.shields.io/badge/Join%20my%20Telegram%20group-2CA5E0?style=for-the-badge&logo=telegram&labelColor=db44ad&color=5e2775"></a>

This Go program applies a lifetime patch to PowerShell to disable ETW (Event Tracing for Windows) and AMSI (Antimalware Scan Interface) protections.

### INFO
The program modifies the PowerShell profile (`Microsoft.PowerShell_profile.ps1`) to apply two patches:

1. **AMSI Patch**: Disables AMSI by modifying the `AmsiScanBuffer` function, ```{ 0x31, 0xC0, 0xC3 }```.
2. **ETW Patch**: Modifies the `EtwEventWrite` function in `ntdll.dll` to prevent event tracing, ```{ 0xC3 }```.
3. Sets File attributes to Hidden and System to : `Microsoft.PowerShell_profile.ps1`.

### Effect: Once applied, PowerShell sessions initiated afterward will have AMSI and ETW bypassed.

- Made by codepulze aka evilbytecode.

## Detections:
![image](https://github.com/EvilBytecode/Lifetime-Amsi-EtwPatch/assets/151552809/57cbd173-922c-4f6a-ada7-e086ed4f4977)
https://www.virustotal.com/gui/file/e1f4539b28df895d02f361143d04f025e36668a9373985ef27b324431f68a0f5


## License
This project is licensed under the MIT License. See the LICENSE file for details.