# powershell

built on .NET framework and now .NET core.
its focused around objects enabling rich squences to be created which can perform complex tasks

syntax = Verb-Noun

when you type ls or dir etc these are not the cmdlets
 - the command let is Get-ChildItem (ls is an alias)


 Get-Alias will spit out all the alias for the cmdlets


 Powershell works with c# objects

```
PS C:\Users\imasi\Documents\Programming> Get-ChildItem | Select-Object Name -First 1

Name
----
eecs3101

```

```
PS C:\Users\imasi\Documents\Programming> Get-ChildItem | Select-Object -Index 0 | Get-Member


   TypeName: System.IO.DirectoryInfo

Name                      MemberType     Definition
----                      ----------     ----------
LinkType                  CodeProperty   System.String LinkType{get=GetLinkType;}
Mode                      CodeProperty   System.String Mode{get=Mode;}
Target                    CodeProperty   System.Collections.Generic.IEnumerable`1[[System.String, mscorlib, Version=...
Create                    Method         void Create(), void Create(System.Security.AccessControl.DirectorySecurity ...
CreateObjRef              Method         System.Runtime.Remoting.ObjRef CreateObjRef(type requestedType)
CreateSubdirectory        Method         System.IO.DirectoryInfo CreateSubdirectory(string path), System.IO.Director...
Delete                    Method         void Delete(), void Delete(bool recursive)
EnumerateDirectories      Method         System.Collections.Generic.IEnumerable[System.IO.DirectoryInfo] EnumerateDi...
EnumerateFiles            Method         System.Collections.Generic.IEnumerable[System.IO.FileInfo] EnumerateFiles()...
EnumerateFileSystemInfos  Method         System.Collections.Generic.IEnumerable[System.IO.FileSystemInfo] EnumerateF...
Equals                    Method         bool Equals(System.Object obj)
GetAccessControl          Method         System.Security.AccessControl.DirectorySecurity GetAccessControl(), System....
GetDirectories            Method         System.IO.DirectoryInfo[] GetDirectories(), System.IO.DirectoryInfo[] GetDi...
GetFiles                  Method         System.IO.FileInfo[] GetFiles(string searchPattern), System.IO.FileInfo[] G...
GetFileSystemInfos        Method         System.IO.FileSystemInfo[] GetFileSystemInfos(string searchPattern), System...
GetHashCode               Method         int GetHashCode()
GetLifetimeService        Method         System.Object GetLifetimeService()
GetObjectData             Method         void GetObjectData(System.Runtime.Serialization.SerializationInfo info, Sys...
GetType                   Method         type GetType()
InitializeLifetimeService Method         System.Object InitializeLifetimeService()
MoveTo                    Method         void MoveTo(string destDirName)
Refresh                   Method         void Refresh()
SetAccessControl          Method         void SetAccessControl(System.Security.AccessControl.DirectorySecurity direc...
ToString                  Method         string ToString()
PSChildName               NoteProperty   string PSChildName=eecs3101
PSDrive                   NoteProperty   PSDriveInfo PSDrive=C
PSIsContainer             NoteProperty   bool PSIsContainer=True
PSParentPath              NoteProperty   string PSParentPath=Microsoft.PowerShell.Core\FileSystem::C:\Users\imasi\Do...
PSPath                    NoteProperty   string PSPath=Microsoft.PowerShell.Core\FileSystem::C:\Users\imasi\Document...
PSProvider                NoteProperty   ProviderInfo PSProvider=Microsoft.PowerShell.Core\FileSystem
Attributes                Property       System.IO.FileAttributes Attributes {get;set;}
CreationTime              Property       datetime CreationTime {get;set;}
CreationTimeUtc           Property       datetime CreationTimeUtc {get;set;}
Exists                    Property       bool Exists {get;}
Extension                 Property       string Extension {get;}
FullName                  Property       string FullName {get;}
LastAccessTime            Property       datetime LastAccessTime {get;set;}
LastAccessTimeUtc         Property       datetime LastAccessTimeUtc {get;set;}
LastWriteTime             Property       datetime LastWriteTime {get;set;}
LastWriteTimeUtc          Property       datetime LastWriteTimeUtc {get;set;}
Name                      Property       string Name {get;}
Parent                    Property       System.IO.DirectoryInfo Parent {get;}
Root                      Property       System.IO.DirectoryInfo Root {get;}
BaseName                  ScriptProperty System.Object BaseName {get=$this.Name;}
```

Get-Command * gives us all the commands we can run on the device
Get-Command *process* gives us all the commands for the current processes


The 2 main command we will need to use powershell
 - Get-Command
 - Get-Help 

