﻿---
title: about_History
description: 
keywords: powershell, cmdlet
author: jpjofre
manager: carolz
ms.date: 2016-09-27
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
title: about_History
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
---
# About History
## about_History
# TOPIC

about_History

# SHORT DESCRIPTION

Describes how to get and run commands in the command history.

# LONG DESCRIPTION

When you enter a command at the command prompt, Windows PowerShell
saves the command in the command history. You can use the commands
in the history as a record of your work. And, you can recall and run the
commands from the command history.

History Cmdlets
Windows PowerShell has a set of cmdlets that manage the command history.

Cmdlet (Alias)       Description
-------------------  ------------------------------------------
Get-History (h)      Gets the command history.

Invoke-History (r)   Runs a command in the command history.

Add-History          Adds a command to the command history.

Clear-History (clh)  Deletes commands from the command history.

Keyboard Shortcuts for Managing History
In the Windows PowerShell console, you can use the following shortcuts
to manage the command history.

For other host applications, see the product documentation.

Use this key      To perform this action
-------------     ----------------------------------------------
UP ARROW          Displays the previous command.

DOWN ARROW        Displays the next command.

F7                Displays the command history.
To hide the history, press ESC.

F8                Finds a command. Type one or more characters,
and then press F8. For the next instance,
press F8 again.

F9                Find a command by history ID. Type the history
ID, and then press F9. To find the ID, press F7.

MaximumHistoryCount
The $MaximumHistoryCount preference variable determines the maximum
number of commands that Windows PowerShell saves in the command history.
The default value is 4096, meaning that Windows PowerShell saves the 4096
most recent commands, but you can change the value of the variable.

For example, the following command lowers the $MaximumHistoryCount to
100 commands:

$MaximumHistoryCount = 100

To apply the setting, restart Windows PowerShell.

To save the new variable value for all your Windows PowerShell
sessions, add the assignment statement to a Windows PowerShell profile.
For more information about profiles, see about_Profiles
(http://go.microsoft.com/fwlink/?LinkID=113729).

For more information about the $MaximumHistoryCount preference
variable, see about_Preference_Variables
(http://go.microsoft.com/fwlink/?LinkID=113248).

NOTE: In Windows PowerShell 2.0, the default value of the $MaximumHistoryCount
preference variable is 64.

Order of Commands in the History
Commands are added to the history when the command finishes executing,
not when the command is entered. If commands take some time to be
completed, or if the commands are executing in a nested prompt, the
commands might appear to be out of order in the history. (Commands
that are executing in a nested prompt are completed only when you exit
the prompt level.)

# SEE ALSO

about_Line_Editing
about_Preference_Variables
about_Profiles
about_Variables
