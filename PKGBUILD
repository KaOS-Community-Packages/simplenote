pkgname=simplenote
pkgver=1.0.3
pkgrel=1
pkgdesc="The simplest way to keep notes."
arch=('x86_64')
url="https://github.com/Automattic/simplenote-electron"
license=('GPL2')
depends=('libnotify' 'alsa-lib' 'gconf' 'gtk2' 'nss' 'libxtst')
md5sums=('a5be9fbb1bab65d454000291d3d3ecae')
source=("https://github.com/Automattic/simplenote-electron/releases/download/v$pkgver/simplenote-$pkgver.deb")


package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  install -dm755 ${pkgdir}/usr/bin
  ln -s ${pkgdir}/usr/share/${pkgname}/${pkgname} ${pkgdir}/usr/bin/${pkgname}
  rm -r $pkgdir/usr/share/doc
}
