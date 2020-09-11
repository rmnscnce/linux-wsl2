Linux-WSL2 README
---
To use the kernel image on WSL2, you have to follow these instructions:

1. Create a directory for kernel image (preferably in the partition containing
Windows files (%SystemDrive%), or in the user's home folder (%UserProfile%))

2. Shutdown all WSL instances using `wsl --shutdown`

3. Copy the kernel image to the directory that was made before

4. Enable the custom kernel image in WSL2 by configuring through
%UserProfile%\.wslconfig:

`` [wsl2]
`` kernel=<DriveLetter>\\path\\to\\kernel_image

5. Restart the Linux Subsystem service using `Restart-Service` LxssManager` on
PowerShell with administrator privileges

6. Start the WSL2 distro!
