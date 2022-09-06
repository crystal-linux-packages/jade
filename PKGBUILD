# Maintainer: Matt C <matt[at]getcryst[dot]al>

pkgname=jade
pkgver=1.0.8
pkgrel=1
pkgdesc="Scriptable backend & TUI Installer for Crystal Linux"
license=('GPLv3')
arch=('x86_64')
url="https://github.com/crystal-linux/$pkgname"
license=('GPL')
source=("git+$url#tag=v$pkgver")
sha256sums=('SKIP')
depends=('parted')
makedepends=('cargo')

build() {
    cd ${srcdir}/${pkgname}
    cargo build --release
}

package() {
    mkdir -p $pkgdir/usr/bin
    chmod +x ${srcdir}/jade/target/release/jade
    cp ${srcdir}/jade/target/release/jade  $pkgdir/usr/bin/.
}
