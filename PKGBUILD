_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=1.16.2
pkgrel=1
pkgdesc="Secure Git credential storage for Windows with support for Visual Studio Team Services, GitHub, and Bitbucket multi-factor authentication"
arch=('any')
url='https://github.com/Microsoft/Git-Credential-Manager-for-Windows'
license=('MIT')
source=("https://github.com/Microsoft/Git-Credential-Manager-for-Windows/releases/download/v${pkgver}/gcmw-v${pkgver}.zip")
depends=('git')
install="${pkgname}.install"
sha256sums=('36a0eabf0469e3f0092a06606d2c0c892009b769decda2b5aea3bed8dadaa63d')

build() {
    cd "${srcdir}"
	rm gcmw-v${pkgver}.zip
    rm install.cmd
    rm README.md
}

package() {
    cd "${srcdir}"
    install -Dm644 LICENSE.TXT "${pkgdir}/usr/share/licenses/${_realname}/LICENSE"
	rm LICENSE.TXT
	mkdir -p ${pkgdir}/usr/lib/git-core
	cp * "${pkgdir}/usr/lib/git-core"
}
