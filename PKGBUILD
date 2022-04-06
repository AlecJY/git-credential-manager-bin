_realname='git-credential-manager-core'
pkgname="${_realname}-bin"
pkgver=2.0.696
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/GitCredentialManager/git-credential-manager'
license=('MIT')
source=("https://github.com/GitCredentialManager/git-credential-manager/releases/download/v${pkgver}/gcmcore-win-x86-${pkgver}.zip")
depends=('git')
conflicts=('git-credential-manager-bin')
install="${pkgname}.install"
sha256sums=('9c80110b4ff0f8e30d572431ee612fc57f398019f83cecb617ad32bb9cb5cacd')

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
