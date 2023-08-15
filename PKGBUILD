_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=2.3.1
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/git-ecosystem/git-credential-manager'
license=('MIT')
source=("https://github.com/git-ecosystem/git-credential-manager/releases/download/v${pkgver}/gcm-win-x86-${pkgver}.zip")
depends=('git')
replaces=('git-credential-manager-core-bin')
conflicts=('git-credential-manager-core-bin')
install="${pkgname}.install"
sha256sums=('32d343a59eb21083c67397a248272c1bc9323e5f4cc5c7f86d5a5f58ed995136')

build() {
    cd "${srcdir}"
    rm gcm-win-x86-${pkgver}.zip
}

package() {
    cd "${srcdir}"
    install -Dm644 NOTICE "${pkgdir}/usr/share/licenses/${_realname}/LICENSE"
    rm NOTICE
    mkdir -p ${pkgdir}/usr/lib/git-core
    cp * "${pkgdir}/usr/lib/git-core"
}
