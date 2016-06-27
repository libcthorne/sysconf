# Manual

* Use the "Screen Display" tool to set monitor position.

# Automated

```
# Hide launcher by default
gsettings set org.compiz.unityshell:/org/compiz/profiles/unity/plugins/unityshell/ launcher-hide-mode 1

# Set launcher icons to 32px
gsettings set org.compiz.unityshell:/org/compiz/profiles/unity/plugins/unityshell/ icon-size 32

# Setup workspaces
gsettings set org.compiz.core:/org/compiz/profiles/unity/plugins/core/ hsize 4
gsettings set org.compiz.core:/org/compiz/profiles/unity/plugins/core/ vsize 3

# Disable startup drum sound (http://askubuntu.com/a/186120)
echo "[com.canonical.unity-greeter]
play-ready-sound = false" | sudo tee --append /usr/share/glib-2.0/schemas/50_unity-greeter.gschema.override
sudo glib-compile-schemas /usr/share/glib-2.0/schemas/

# Lock on lid close
echo "HandleLidSwitchDocked=lock" | sudo tee --append /etc/systemd/logind.conf

# Swap CAPS and CTRL
# immediately
setxkbmap -option ctrl:nocaps
# permanently
sudo sed -i 's/XKBOPTIONS=""/XKBOPTIONS="ctrl:nocaps"/' /etc/default/keyboard
```
