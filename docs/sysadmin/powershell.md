# Powershell

## Execution Policy

### Available Scopes:

- MachinePolicy
- UserPolicy
- Process
- CurrentUser
- LocalMachine

### Available Policies

- Restricted
- AllSigned
- RemoteSigned
- Unrestricted

### Commands

```
# List current policy for each scope
Get-ExecutionPolicy -List

# Change the policy for a given scope
Set-ExecutionPolicy -Scope <ScopeName> -ExecutionPolicy <PolicyName>
```
