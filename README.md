# install-age
https://technotim.live/posts/install-age/
AGE_LATEST_VERSION=$(curl -s "https://api.github.com/repos/FiloSottile/age/releases/latest" | grep -Po '"tag_name": "v\K[0-9.]+')
AGE_LATEST_VERSION=$(curl -s "https://api.github.com/repos/FiloSottile/age/releases/latest" | grep -Po '"tag_name": "v\K[0-9.]+')

tar xf age.tar.gz

sudo mv age/age /usr/local/bin
sudo mv age/age-keygen /usr/local/bin

rm -rf age.tar.gz
rm -rf age

age -version
age-keygen -version

# Uninstall:
sudo rm -rf /usr/local/bin/age
sudo rm -rf /usr/local/bin/age-keygen

#


#
