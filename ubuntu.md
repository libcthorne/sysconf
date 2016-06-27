# Manual

* Use the "Screen Display" tool to set monitor position.

# Automated

```
BACKGROUND_URL="http://thewallpaper.co/wp-content/uploads/2016/03/space-stars-hd-wallpaper-download-stars-images-free-hd-images-abstract-widescreen-1920x1080.jpg"

# Download and set background image
wget $BACKGROUND_URL -O background-image
gsettings set org.gnome.desktop.background picture-uri file:///home/$(whoami)/background-image

# Hide Unity launcher by default
gsettings set org.compiz.unityshell:/org/compiz/profiles/unity/plugins/unityshell/ launcher-hide-mode 1

# Set Unity launcher icons to 32px
gsettings set org.compiz.unityshell:/org/compiz/profiles/unity/plugins/unityshell/ icon-size 32

# Set Unity launcher icons
gsettings set com.canonical.Unity.Launcher favorites "['application://ubiquity.desktop', 'application://org.gnome.Nautilus.desktop', 'application://firefox.desktop', 'application://emacs.desktop', 'application://anki.desktop', 'application://skype.desktop', 'unity://running-apps', 'unity://devices']"

# Setup workspaces
gsettings set org.compiz.core:/org/compiz/profiles/unity/plugins/core/ hsize 4
gsettings set org.compiz.core:/org/compiz/profiles/unity/plugins/core/ vsize 3

# Disable startup drum sound (http://askubuntu.com/a/186120)
printf "[com.canonical.unity-greeter]\nplay-ready-sound = false" | sudo tee /usr/share/glib-2.0/schemas/50_unity-greeter.gschema.override
sudo glib-compile-schemas /usr/share/glib-2.0/schemas/

# Lock on lid close
printf "HandleLidSwitch=lock\nHandleLidSwitchDocked=lock" | sudo tee --append /etc/systemd/logind.conf

# Disable prompt for what to do when mounting media
gsettings set org.gnome.desktop.media-handling autorun-never true

# Swap CAPS and CTRL
# immediately
setxkbmap -option ctrl:nocaps
# permanently
sudo sed -i 's/XKBOPTIONS=""/XKBOPTIONS="ctrl:nocaps"/' /etc/default/keyboard
```
