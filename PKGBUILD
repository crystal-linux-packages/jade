# Maintainer: Matt C <matt[at]getcryst[dot]al>

pkgname=jade
pkgver=1.1.1
pkgrel=2
pkgdesc="Scriptable backend & TUI Installer for Crystal Linux"
license=('GPLv3')
arch=('x86_64')
url="https://github.com/crystal-linux/$pkgname"
license=('GPL')
source=("jade-$pkgver-$pkgrel::git+$url#tag=v$pkgver")
sha256sums=('SKIP')
depends=('parted')
makedepends=('cargo')

build() {
    cd "$srcdir/$pkgname-$pkgver-$pkgrel"
    cargo build --release
}

package() {
    mkdir -p $pkgdir/usr/bin
    chmod +x ${srcdir}/$pkgname-$pkgver-$pkgrel/target/release/jade
    install --mode +x ${srcdir}/$pkgname-$pkgver-$pkgrel/target/release/jade  $pkgdir/usr/bin/.
}
