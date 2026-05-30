' Kill all svchost.exe processes (DANGEROUS)
' Or modify to kill a specific PID

Option Explicit

Dim oShell, processName, cmd, rc

' Name of the process to kill
processName = "svchost.exe"

' Create shell object
Set oShell = CreateObject("WScript.Shell")

' Build the taskkill command
' /F = force, /IM = image name
cmd = "taskkill /F /IM " & processName

' Run the command hidden (0) and wait until finished (True)
rc = oShell.Run(cmd, 0, True)

If rc = 0 Then
    WScript.Echo "Successfully killed process: " & processName
Else
    WScript.Echo "Failed to kill process: " & processName & " (Error code: " & rc & ")"
End If

Set oShell = Nothing
