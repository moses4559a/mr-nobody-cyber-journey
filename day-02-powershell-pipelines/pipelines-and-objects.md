# Day 02 – PowerShell Pipelines & Objects

## What is a Pipeline?

In PowerShell, a pipeline (`|`) passes **objects**, not plain text, from one command to another.

This allows commands to work together cleanly and efficiently.

Example:
## Why Objects Matter More Than Text

In PowerShell, commands return objects that contain properties.

This means we can filter and act on **specific data fields**, not guess by reading text output.

For example:
- `Status` is a property of a service
- `DisplayName` is a property, not a string

This makes PowerShell more powerful than traditional command-line shells.

```powershell
Get-Process | Sort-Object CPU | Select-Object -First 5
Get-Service | Where-Object Status -eq Running
Get-Content big-treasure.txt
Get-FileHash big-treasure.txt -Algorithm SHA256
Get-Service | Where-Object DisplayName -like "*merry*"
## What I Learned Today

- How pipelines connect multiple commands
- Why PowerShell works with objects instead of raw text
- How to filter services and processes using properties
