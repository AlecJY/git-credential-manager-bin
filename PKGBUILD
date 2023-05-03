_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=2.1.0
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
sha256sums=('50addbb42e53bb944576efcc2ab3de7947064f6273b0ed9cfb0833e9566b062c')

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
