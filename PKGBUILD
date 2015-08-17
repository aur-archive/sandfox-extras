# Maintainer: Gently <toddrpartridge@gmail.com>

pkgname=sandfox-extras
pkgver=1.10
pkgrel=1
pkgdesc="Extras for sandfox: a Desktop-menu file and systemd cleanup services"
arch=('any')
url="http://linuxtidbits.wordpress.com/2013/02/24/sandfoxing-firefox-imho-necessary/"
license=('GPL')
depends=('sandfox')
optdepends=('gksu: firefox launch from menu sudo prompt')
source=('jailed-firefox'
        'jailed-firefox.desktop'
        'jailed-firefox.svg'
        'sandfox-rmdir-boot.service'
        'sandfox-unmount-poweroff.service')
noextract=()
md5sums=('1c7d33adb89cc78c04f77c7007209890'
         '38b0253883a0e85d2ed99b0c5e5c6509'
         '59b6715c4e69c57c9108e5af34f2b26b'
         '3d948b3b48d6c6062bb144461e47d34b'
         '9c9e08a4a8258480592eea24548bde55')

package() {
  install -Dm755 jailed-firefox ${pkgdir}/usr/bin/jailed-firefox
	install -Dm755 jailed-firefox.desktop     \
    ${pkgdir}/usr/share/applications/jailed-firefox.desktop
  install -Dm644 jailed-firefox.svg         \
    ${pkgdir}/usr/share/pixmaps/jailed-firefox.svg
  install -Dm644 sandfox-rmdir-boot.service \
    ${pkgdir}/etc/systemd/system/sandfox-rmdir-boot.service
  install -Dm644 sandfox-unmount-poweroff.service \
    ${pkgdir}/etc/systemd/system/sandfox-unmount-poweroff.service
}
