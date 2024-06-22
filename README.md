# Lifetime-Amsi-EtwPatch

This Go program applies a lifetime patch to PowerShell to disable ETW (Event Tracing for Windows) and AMSI (Antimalware Scan Interface) protections.

### INFO
The program modifies the PowerShell profile (`Microsoft.PowerShell_profile.ps1`) to apply two patches:

1. **AMSI Patch**: Disables AMSI by modifying the `AmsiScanBuffer` function.
2. **ETW Patch**: Modifies the `EtwEventWrite` function in `ntdll.dll` to prevent event tracing.
3. Sets File attributes to Hidden and System to : `Microsoft.PowerShell_profile.ps1`.

### Effect: Once applied, PowerShell sessions initiated afterward will have AMSI and ETW bypassed.

- Made by codepulze aka evilbytecode.
