_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=1.20.0
pkgrel=1
pkgdesc="Secure Git credential storage for Windows with support for Visual Studio Team Services, GitHub, and Bitbucket multi-factor authentication"
arch=('any')
url='https://github.com/Microsoft/Git-Credential-Manager-for-Windows'
license=('MIT')
source=("https://github.com/Microsoft/Git-Credential-Manager-for-Windows/releases/download/${pkgver}/gcmw-v${pkgver}.zip")
depends=('git')
install="${pkgname}.install"
sha256sums=('523847459aef94bf45e15c08ab67c1c23b6dcb563b2cbda956c04dc491f82cdb')

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
