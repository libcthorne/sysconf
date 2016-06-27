# Software

## Ubuntu 15.04 (16/06/27)

```
# Uncomment source repositories for build-dep
sudo sed -i 's/# deb-src/deb-src/g' /etc/apt/sources.list
# Update sources
sudo apt-get update
```

```
# Install Google Chrome
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt-get update
sudo apt-get -y install -fg oogle-chrome-stable
```
```
# Install Emacs 24.5
sudo DEBIAN_FRONTEND=noninteractive apt-get -y build-dep emacs24
wget ftp://ftp.gnu.org/pub/gnu/emacs/emacs-24.5.tar.gz
tar -zxvf emacs-24.5.tar.gz
cd emacs-24.5
./configure
make
sudo make install
```

* Mozilla Firefox (*installed by default*)
* Google Chrome
* GNU Emacs 24.4
* Anki (from source)
* Android Studio
* Skype
* VMware Player
* GIMP
* Dropbox
* Steam
* LibreOffice
* Transmission
* Unity Tweak Tool
* Ubuntu Tweak
* Tweak Tool
* Evince Document Viewer
* redshift
* Node v5.0.0
* npm 3.9.5
* rbenv 0.4.0 (Ruby 2.2.3 and 2.3.0 installed)
* Rails 4.2.6
* adbcontrol
* CompizConfig
* SMPlayer
* Spotify
* Visual Studio Code
* Eclipse
* LINE (Wine)
* Audacity
* pgAdmin / postgres
