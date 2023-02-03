Ok så nå tror jeg det funker her...

Valgte fra arcolinuxd-v23.01.03 å starte UTEN nvidia drivere (og uten nouveau).
Installerte linux-lts kernel og intel-ucode
Med sddm og awesome + et utvalg apper og utils (kun upower og noen få hw-discovery tools)

Etter dette, fulgte Nvidia_Optimus på wiki archlinux som bestod i å installere nvidia-lts, nvidia-settings, nvidia-utils og nvidia-prime

Etter reboot kunne jeg sjekke at det systemet iallfal ser ok ut med denne kommando:

` glxinfo | grep "OpenGL renderer"
vil vise *intel* graphics

` prime-run glxinfo | grep "OpenGL renderer"
vil vise *NVIDIA* graphics


https://wiki.archlinux.org/title/NVIDIA
https://wiki.archlinux.org/title/NVIDIA_Optimus
https://wiki.archlinux.org/title/PRIME#PRIME_render_offload


