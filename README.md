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


domaine

# Install Sops
https://technotim.live/posts/secret-encryption-sops/

SOPS_LATEST_VERSION=$(curl -s "https://api.github.com/repos/getsops/sops/releases/latest" | grep -Po '"tag_name": "v\K[0-9.]+')

curl -Lo sops.deb "https://github.com/getsops/sops/releases/download/v${SOPS_LATEST_VERSION}/sops_${SOPS_LATEST_VERSION}_amd64.deb"

sudo apt --fix-broken install ./sops.deb

rm -rf sops.deb

sops -version

# Unistall
sudo apt remove sops
