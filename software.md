# Software

## Notes

* If available, copy Dropbox folder to ~/Dropbox before opening Dropbox to avoid unnecessary downloads.

## Ubuntu 16.04 (16/06/27)

```
# Uncomment source repositories for build-dep
sudo sed -i 's/# deb-src/deb-src/g' /etc/apt/sources.list
# Update sources
sudo apt-get update
# Install dependencies
sudo apt-get -y install build-essential
# Enable 32 bit architecture (primarily for Wine)
sudo dpkg --add-architecture i386 
```

```
# Install Git
sudo apt -y install git
# Configure Git
git config --global user.name "Christopher Thorne"
git config --global user.email "libcthorne@gmail.com"
```

```
# Install Markdown
sudo apt-get -y install markdown
```

```
# Install NVM
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.31.2/install.sh | bash
. .bashrc
# Install NodeJS 5.0 (and npm 3.3.6)
nvm install 5.0
```

```
# Install RVM with latest Ruby+Rails
command curl -sSL https://rvm.io/mpapis.asc | gpg2 --import -
curl -L https://get.rvm.io | bash -s stable --autolibs=enabled --ruby --rails
. ~/.rvm/scripts/rvm
# Install Ruby 2.2.3+2.3.0+
rvm install 2.2.3 2.3.0
# Use Ruby 2.3.0 as default Ruby version
rvm --default use 2.3.0
# Add rvm init to .bashrc for non-login shell
echo '[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm" # Load RVM into a shell session *as a function*' >> ~/.bashrc
```

```
# Install Wine
sudo add-apt-repository -y ppa:wine/wine-builds
sudo apt-get update
sudo apt-get -y install --install-recommends winehq-devel
```

```
# Install Dropbox
sudo apt-get -y install nautilus-dropbox
```

```
# Install Java
sudo add-apt-repository -y ppa:webupd8team/java
sudo apt-get update
# accept license
echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | sudo debconf-set-selections
sudo apt-get -y install oracle-java8-installer oracle-java8-set-default
```

```
# Install Flash Player
sudo apt-get -y install flashplugin-installer
```

```
# Install GParted
sudo apt -y install gparted
```

```
# Install LaTeX
sudo apt-get -y install texlive-full texstudio
```

```
# Install Google Chrome
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt-get update
sudo apt-get -y install google-chrome-stable
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
cd -
rm -rf emacs-24.5
```

```
# Install Anki
sudo apt-get -y install python-qt4 mplayer lame libportaudio2 python-sqlalchemy pyqt4-dev-tools
git clone https://github.com/dae/anki.git
cd anki
tools/build_ui.sh
sudo make install
cd -
```

```
# Install Skype
sudo add-apt-repository "deb http://archive.canonical.com/ $(lsb_release -sc) partner"
sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get -y install skype
```

```
# Install Android Studio 2.1.2
wget https://dl.google.com/dl/android/studio/ide-zips/2.1.2.0/android-studio-ide-143.2915827-linux.zip
sudo unzip android-studio-ide-143.2915827-linux.zip -d /opt
echo 'PATH="/opt/android-studio/bin:$PATH"' >> .profile
. .profile
```

```
# Install GIMP
sudo add-apt-repository -y ppa:otto-kesselgulasch/gimp
sudo apt-get update
sudo apt-get -y install gimp
```

```
# Install Steam
# accept license
echo 'steam steam/question select I AGREE' | sudo debconf-set-selections
echo 'steam steam/licence note ' | sudo debconf-set-selections
sudo apt-get -y install steam
```

```
# Install Audacity
sudo apt-get -y install audacity
```

```
# Install SMPlayer
sudo add-apt-repository -y ppa:rvm/smplayer
sudo apt-get update
sudo apt-get -y install smplayer smplayer-themes smplayer-skins
```

```
# Install PostgreSQL
sudo apt-get install postgresql postgresql-contrib
```

```
# Install Spotify
# 1. Add the Spotify repository signing key to be able to verify downloaded packages
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BBEBDCB318AD50EC6865090613B00F1FD2C19886
# 2. Add the Spotify repository
echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list
# 3. Update list of available packages
sudo apt-get update
# 4. Install Spotify
sudo apt-get install spotify-client
```

```
# Install Redshift
sudo apt-get -y install redshift redshift-gtk
printf "[redshift]\nlocation-provider=manual\n\n[manual]\nlat=51.5\nlon=0.12\n" | sudo tee ~/.config/redshift.conf
```

## Ubuntu 15.04 (16/06/27)

### Installed
* Google Chrome
* GNU Emacs 24.4
* Anki (from source)
* Android Studio
* Skype
* GIMP
* Dropbox
* Steam
* redshift
* Node v5.0.0
* npm 3.9.5
* rbenv 0.4.0 (Ruby 2.2.3 and 2.3.0 installed)
* Rails 4.2.6
* adbcontrol
* SMPlayer
* Spotify
* Visual Studio Code
* Eclipse
* LINE (Wine)
* Audacity
* pgAdmin / postgres
* VMware Player
* Unity Tweak Tool
* Ubuntu Tweak
* Tweak Tool
* CompizConfig

### Frequently used defaults
* Mozilla Firefox
* Transmission
* Evince Document Viewer
* LibreOffice
