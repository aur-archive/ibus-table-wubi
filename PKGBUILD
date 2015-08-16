# Contributor: Lee.MaRS<leemars at gmail.com>
# Maintainer: Daniel J Griffiths <ghost1227@archlinux.us>

pkgname=ibus-table-wubi
pkgver=1.2.0.20091227
pkgrel=2
pkgdesc='The Wubi Input Method of tables engines for IBus. (deprecated)'
arch=('i686' 'x86_64')
url='http://code.google.com/p/ibus/'
license=('LGPL')
depends=('ibus-table>=1.2.0')
provides=('ibus-table-wubi=1.2.0')
makedepends=('ibus-table-extraphrase=1.2.0')
source=("http://ibus.googlecode.com/files/${pkgname}-${pkgver}.tar.gz")
md5sums=('3035c499c10362ff426468de1b66ee80')

build() {
  cd ${pkgname}-${pkgver}

  ./autogen.sh

  ./configure \
    --prefix=/usr \
    --libexecdir=/usr/lib/ibus \
    --enable-wubi86 \
    --enable-wubi98 \
    --enable-extra-phrases

  make
}

package() {
  cd ${pkgname}-${pkgver}

  make DESTDIR=${pkgdir} install
}
