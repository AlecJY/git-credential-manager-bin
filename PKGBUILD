_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=2.0.866
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/GitCredentialManager/git-credential-manager'
license=('MIT')
source=("https://github.com/GitCredentialManager/git-credential-manager/releases/download/v${pkgver}/gcm-win-x86-${pkgver}.zip")
depends=('git')
replaces=('git-credential-manager-core-bin')
conflicts=('git-credential-manager-core-bin')
install="${pkgname}.install"
sha256sums=('7fc432a3cca7799f91d4c488ec3b63ad6fa1661cc99e291874fc653188131837')

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
