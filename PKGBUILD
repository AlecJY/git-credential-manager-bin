_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=1.18.5
pkgrel=1
pkgdesc="Secure Git credential storage for Windows with support for Visual Studio Team Services, GitHub, and Bitbucket multi-factor authentication"
arch=('any')
url='https://github.com/Microsoft/Git-Credential-Manager-for-Windows'
license=('MIT')
source=("https://github.com/Microsoft/Git-Credential-Manager-for-Windows/releases/download/${pkgver}/gcmw-v${pkgver}.zip")
depends=('git')
install="${pkgname}.install"
sha256sums=('dd058fe314329d0fa5435925503a72a394eedfb4f30268e3c6423a3121589ea7')

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
