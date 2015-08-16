# Maintainer: Joel Teichroeb <joel@teichroeb.net>

pkgname=libinput
pkgver=0.1.0
pkgrel=2
pkgdesc='A library to handle input devices in Wayland compositors'
arch=('i686' 'x86_64')
url='http://freedesktop.org/wiki/Software/libinput/'
license=('MIT')
depends=('mtdev' 'udev' 'libevdev')
source=("http://www.freedesktop.org/software/$pkgname/$pkgname-$pkgver.tar.xz")
sha1sums=('4d38a9c3aea30f98c53108c7e91364427ed0015a')

build() {
  cd $pkgname-$pkgver

  ./configure --prefix=/usr
  make
}

package() {
  cd $pkgname-$pkgver

  make DESTDIR="$pkgdir" install
}
