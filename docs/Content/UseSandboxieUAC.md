# Use Sandboxie UAC

**UseSandboxieUAC** is a global sandbox setting in [Sandboxie Ini](SandboxieIni.md) available since v1.16.0/5.71.0. Sandboxie intercepts and manages UAC elevation requests from sandboxed applications when enabled.

Usage:

```
   .
   .
   .
   [GlobalSettings]
   UseSandboxieUAC=y
```

[Sandboxie UAC Prompt]
----------------------------------
| Sandbox: DefaultBox            |
| Program: Start.exe             |
|                                |
| [Yes] - Grant real admin       |
| [No]  - Grant fake admin       |
| [Cancel] - Deny request        |
----------------------------------

## Behavior and Configuration

By default, Sandboxie follows the system's UAC configuration - when User Account Control is set to prompt on the secure desktop, Sandboxie's UAC prompts will also appear there. This behavior can be modified using the [PromptOnSecureDesktop](PromptOnSecureDesktop.md) setting to prevent sandboxed applications from displaying elevation prompts on the secure desktop.

## Related Configuration

This setting corresponds to the GUI option in **Sandboxie Plus** under the following path:

**Options** > **Global Settings** > **Advanced Config**: _Use Sandboxie's own enhanced UAC prompt (experimental)_.