# How to install Docker on Windows 10 Home
If you are trying to install Docker on Windows 10 Home, probably you could run into this issue:
Docker Desktop requires Windows 10 Pro or Enterprise version 15063 or Windows 10 Home (19018+).

## Solution

### Install HyperV
1. Download batch files included (**InstallContainers.bat**, **InstallHyperV.bat**) on this repo.
2. Run `InstallHyperV.bat` in administrator mode.
3. Run `InstallContainers.bat` in administrator mode.
4. Restart your computer.

### Configure Edition on Regedit
1. Open the Registry Editor (*Windows + R*, then write *regedit*)
2. Go to `\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion`
3. Right-Click on `EditionID` and click `Modify`
4. Change value data to `Professional`
5. Press `OK`

**Note:** *No restart windows until you have installed Docker, if you restart your computer you will loose your configuration.*

### Install Docker
1. Get Docker from [here](https://docs.docker.com/docker-for-windows/install/)
2. Run the Docker Desktop Installer.exe file.

### Finally
Review that Docker is running.

I hope this solution helped you to get working the Docker Engine on your Windows 10 Home.
