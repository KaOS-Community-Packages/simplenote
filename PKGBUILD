pkgname=simplenote
pkgver=1.0.0
pkgrel=1
pkgdesc="The simplest way to keep notes."
arch=('x86_64')
url="https://github.com/Automattic/simplenote-electron"
license=('GPL2')
depends=('libnotify' 'alsa-lib' 'gconf' 'gtk2' 'nss')
sha256sums=('c1778a652146a296a98fe2773d6b9fd17eaf9e9199b4aae00e23376af3643c7b')
source=("https://github.com/Automattic/simplenote-electron/releases/download/v$pkgver/simplenote-$pkgver.deb")


package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  install -dm755 ${pkgdir}/usr/bin
  ln -s ${pkgdir}/usr/share/${pkgname}/${pkgname} ${pkgdir}/usr/bin/${pkgname}
  rm -r $pkgdir/usr/share/doc
}
