# ODT
# Microsoft Office Deployment Tool Configuration


Since MS Office is now installed with all applicable packages, user cannot select individual applications (like Word, Excel) to install on a PC.
ODT can be used to securely install only required Office Applcation, hence saving bunch of space of a primary storage device.

Steps:
1. Download latest version of ODT from official Microsoft website: https://www.microsoft.com/en-in/download/details.aspx?id=49117 and extract on a local folder
2. Create a configuration file (config.xml) which indicates required Application from Office Suite and place it in the same folder
3. Run "setup.exe /download config.xml" (this will download the required files)
4. Run "setup.exe /configure config.xml" (this will initiate the installation process)


XML (config.xml):
<Configuration>
	<Add SourcePath="D:\OfficeDW" OfficeClientEdition="64" Channel="PerpetualVL2016">
	<Product ID="ProPlusRetail"  PIDKEY="XXXXX-XXXXX-XXXXX-XXXXX-XXXXX" >
	<Language ID="en-us" />
	
<ExcludeApp ID="Access" />
<ExcludeApp ID="Groove" />
<ExcludeApp ID="InfoPath" />
<ExcludeApp ID="Lync" />
<ExcludeApp ID="OneNote" />
<ExcludeApp ID="OneDrive" />
<ExcludeApp ID="Outlook" />
<ExcludeApp ID="Project" />
<ExcludeApp ID="Publisher" />
<ExcludeApp ID="SharePointDesigner" />
<ExcludeApp ID="Skype" />
<ExcludeApp ID="Skypeforbusiness" />
<ExcludeApp ID="Visio" />
<ExcludeApp ID="Teams" />

      </Product>
  </Add>
     <RemoveMSI All="True" />
    <Display Level="None" AcceptEULA="TRUE" />
 </Configuration>
