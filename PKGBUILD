_realname='git-credential-manager-core'
pkgname="${_realname}-bin"
pkgver=2.0.692
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/GitCredentialManager/git-credential-manager'
license=('MIT')
source=("https://github.com/GitCredentialManager/git-credential-manager/releases/download/v${pkgver}/gcmcore-win-x86-${pkgver}.zip")
depends=('git')
conflicts=('git-credential-manager-bin')
install="${pkgname}.install"
sha256sums=('7b7f4bef34e92ad89c3facddfd9d785af6ad7dce5ca7b06820369f142db33609')

build() {
    cd "${srcdir}"
    rm gcmcore-win-x86-${pkgver}.zip
    rm validatesign.timestamp
}

package() {
    cd "${srcdir}"
    install -Dm644 NOTICE "${pkgdir}/usr/share/licenses/${_realname}/LICENSE"
    rm NOTICE
    mkdir -p ${pkgdir}/usr/lib/git-core
    cp * "${pkgdir}/usr/lib/git-core"
}
