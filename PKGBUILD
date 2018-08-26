_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=1.17.1
pkgrel=1
pkgdesc="Secure Git credential storage for Windows with support for Visual Studio Team Services, GitHub, and Bitbucket multi-factor authentication"
arch=('any')
url='https://github.com/Microsoft/Git-Credential-Manager-for-Windows'
license=('MIT')
source=("https://github.com/Microsoft/Git-Credential-Manager-for-Windows/releases/download/v${pkgver}/gcmw-v${pkgver}.zip")
depends=('git')
install="${pkgname}.install"
sha256sums=('3e4cee79c56f673e4b6c19d6173fa35006816846592e38c03635e1f32ed7691d')

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
