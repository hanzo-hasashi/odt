# ODT
# Microsoft Office Deployment Tool Configuration


Since MS Office is now installed with all applicable packages, user cannot select individual applications (like Word, Excel) to install on a PC.
ODT can be used to securely install only required Office Applcation, hence saving bunch of space of a primary storage device.

Steps:
1. Download latest version of ODT from official Microsoft website: https://www.microsoft.com/en-in/download/details.aspx?id=49117 and extract on a local folder
2. Create a configuration file (config.xml) which indicates required Application from Office Suite and place it in the same folder
3. Run "setup.exe /download config.xml" (this will download the required files)
4. Run "setup.exe /configure config.xml" (this will initiate the installation process)
