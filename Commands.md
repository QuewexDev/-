# When you created CodeSpaces you should run this command:

sudo apt update

# If you need download something then use this:

git clone (link to git)

_Or if you need download file, not entire repository then use this:_

wget (link)

# Download package:

sudo apt install 

_If you need install from flathub repository then run this first:_

_sudo apt install flatpak_
_flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo_

_And reboot the codespace_

_After installing flatpak you can find apps from flathub repository in https://flathub.org/_

# Installing QEMU with VNC Viewer (noVNC)

__Installing qemu first, run this command__

sudo apt install qemu-system-x86-64

__Now downloading noVNC and websockify, run this commands:__

git clone https://github.com/novnc/noVNC.git
git clone https://github.com/novnc/websockify.git

_Done! You installed qemu with noVNC_

# Running noVNC

_You should install noVNC and websockify in one directory_
_For run noVNC, first, you should change your directory into websockify_

cd websockify

_After, you should run this command: _

python3 -m websockify (port where will noVNC running) 127.0.0.1:(vnc port) --web ../noVNC

_And you will see message with said the port is forwarding, and you can go to that port_
