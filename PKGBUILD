_realname='git-credential-manager-core'
pkgname="${_realname}-bin"
pkgver=2.0.632
_buildver=34631
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/microsoft/Git-Credential-Manager-Core'
license=('MIT')
source=("https://github.com/microsoft/Git-Credential-Manager-Core/releases/download/v${pkgver}/gcmcore-win-x86-${pkgver}.${_buildver}.zip")
depends=('git')
conflicts=('git-credential-manager-bin')
install="${pkgname}.install"
sha256sums=('2803bf5cc205a5923395e4b9ed8931387dc52eeb878b3acc9775de732b221116')

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
