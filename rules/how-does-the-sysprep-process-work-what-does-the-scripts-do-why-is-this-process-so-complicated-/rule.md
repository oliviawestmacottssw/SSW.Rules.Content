---
type: rule
title: How does the sysprep process work, what does the scripts do? Why is this process so complicated ?
uri: how-does-the-sysprep-process-work-what-does-the-scripts-do-why-is-this-process-so-complicated-
created: 2009-02-26T02:03:41.0000000Z
authors: []

---


1. SharePoint server can't be renamed after SharePoint is installed
2. Multiple VM's with the same name can't be powered up in the same network
3. So the master.vhd contains:
    1. Windows 2003 server SP2
    2. Visual Studio .NET 2005
    3. Microsoft Office SharePoint Designer
4. When sysprep is ran on the master.vhd, it generalises Windows 2003 server (generate new machine guide, rename computer, etc), the scripts that run also puts "administrator" into the registry so that'd be the name of the next login prompt. A vhd that is in this state is the "sysprep'ed" vhd
5. When it restarts and the user logs in with administrator, it then runs the script to install
    1. SQL Server 2005
    2. Puts MossFarm account into registry
6. After restart - login with MossFarm account and run the scripts to install
    1. SharePoint 2007 sp1
7. Runs Moss\Post\_Build.cmd


