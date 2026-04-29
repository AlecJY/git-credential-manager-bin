_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=2.8.0
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('x86_64')
url='https://github.com/git-ecosystem/git-credential-manager'
license=('MIT')
source=("https://github.com/git-ecosystem/git-credential-manager/releases/download/v${pkgver}/gcm-win-x64-${pkgver}.zip")
depends=('git')
replaces=('git-credential-manager-core-bin')
conflicts=('git-credential-manager-core-bin')
install="${pkgname}.install"
sha256sums=('86c53aaa403d570b11fd48f17a277cd822b41b76c4e6b35f78344ad7c887b6c9')

build() {
    cd "${srcdir}"
    rm gcm-win-x64-${pkgver}.zip
}

package() {
    cd "${srcdir}"
    install -Dm644 NOTICE "${pkgdir}/usr/share/licenses/${_realname}/LICENSE"
    rm NOTICE
    mkdir -p ${pkgdir}/usr/lib/git-core
    cp * "${pkgdir}/usr/lib/git-core"
}
