---
title: "Shutdown computers with PowerShell"
layout: post
---
A couple of days ago I needed some kind of automation to shutdown several computers on my LAN that were also part of the company domain. So I came up with this script that runs as a Scheduled task on my Domain Controller:
<pre class="lang:ps decode:true">$computers = Get-Content C:\computers.txt

for ($i=0; $i -lt $computers.count; $i++) {
    try {
        Stop-Computer -Force -ComputerName $computers[$i]
    }
    catch {
        $ErrorActionPreference = "Continue"
    }
}</pre>
The first row fetches a list of computer names (inside computers.txt there is one name per row)

The <strong>for </strong>then cycles on every computer name and tries to shutdown. If it fails for any reason, the <strong>catch </strong>block makes it continue with the next one.
