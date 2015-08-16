# Maintainer : Martin Wimpress <code@flexion.org>
# Contributor: Giovanni "Talorno" Ricciardi <kar98k.sniper@gmail.com>

pkgname=mate-file-manager-share
pkgver=1.6.0
pkgrel=7
pkgdesc="A Caja extension to quickly share a folder."
url="http://mate-desktop.org"
arch=('i686' 'x86_64' 'armv6h' 'armv7h')
license=('GPL')
depends=('mate-file-manager' 'samba')
makedepends=('mate-common' 'perl-xml-parser')
options=('!emptydirs')
groups=('mate-extra')
source=("http://pub.mate-desktop.org/releases/1.6/${pkgname}-${pkgver}.tar.xz")
sha1sums=('28e8ec54330e41aa44866107c23f48b47ea198e4')

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    PYTHON=/usr/bin/python2 ./autogen.sh \
        --prefix=/usr
    make
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
