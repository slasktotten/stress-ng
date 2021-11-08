# Maintainer: Thomas Wucher <arch (at) thomaswucher (dot) de>
pkgname=stress-ng
pkgver=0.13.06
pkgrel=1
pkgdesc="stress-ng will stress test a computer system in various selectable ways"
arch=('i686' 'x86_64' 'armv7h' 'armv6h' 'aarch64')
url="http://kernel.ubuntu.com/~cking/${pkgname}/"
license=('GPL')
depends=()
depends_x86_64=(intel-ipsec-mb)
source=("stress-ng-master.zip")
sha256sums=('09137c01ac4e8bd9e16c829c2fa2b6a9478454b9440899ce7415c6883555aad0')

build() {
unzip "${source}"
  cd "stress-ng-master"

  make
}

package() {
  cd "stress-ng-master"

  make DESTDIR="${pkgdir}/" install
}
