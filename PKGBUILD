_realname='git-credential-manager-core'
pkgname="${_realname}-bin"
pkgver=2.0.605
_buildver=12951
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/microsoft/Git-Credential-Manager-Core'
license=('MIT')
source=("https://github.com/microsoft/Git-Credential-Manager-Core/releases/download/v${pkgver}/gcmcore-win-x86-${pkgver}.${_buildver}.zip")
depends=('git')
conflicts=('git-credential-manager-bin')
install="${pkgname}.install"
sha256sums=('3433ebedd65fd7b19edbb52410a89621a4e32f00933b8b00f730cf540af04898')

build() {
    cd "${srcdir}"
	rm gcmcore-win-x86-${pkgver}.${_buildver}.zip
    rm validatesign.timestamp
}

package() {
    cd "${srcdir}"
    install -Dm644 NOTICE "${pkgdir}/usr/share/licenses/${_realname}/LICENSE"
	rm NOTICE
	mkdir -p ${pkgdir}/usr/lib/git-core
	cp * "${pkgdir}/usr/lib/git-core"
}
