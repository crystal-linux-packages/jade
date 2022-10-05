# Maintainer: echo -n 'bWF0dEBnZXRjcnlzdC5hbA==' | base64 -d
# Contributor: echo -n 'cmNhbmRhdUBnZXRjcnlzdC5hbA==' | base64 -d

pkgname=jade
pkgver=1.2.0
pkgrel=2
pkgdesc="Scriptable backend & TUI Installer for Crystal Linux"
arch=('x86_64')
url="https://github.com/crystal-linux/${pkgname}"
license=('GPL3')
depends=('parted')
makedepends=('cargo')
source=("${pkgname}-${pkgver}::${url}/archive/v${pkgver}.tar.gz")
sha256sums=('fcf1b168e14c0903572d45b9a16a241a2b72edf2f496745502c7edf24ba3ee62')

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    cargo build --release
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    install -Dm 755 "target/release/${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
}
