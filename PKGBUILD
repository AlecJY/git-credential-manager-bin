_realname='git-credential-manager-core'
pkgname="${_realname}-bin"
pkgver=2.0.498
_buildver=54650
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/microsoft/Git-Credential-Manager-Core'
license=('MIT')
source=("https://github.com/microsoft/Git-Credential-Manager-Core/releases/download/v${pkgver}/gcmcore-win-x86-${pkgver}.${_buildver}.zip")
depends=('git')
conflicts=('git-credential-manager-bin')
install="${pkgname}.install"
sha256sums=('4bb0ef73f0ed9892ae5ac2200389a8a3ee3200e47f0fcf598406caff1c4a6885')

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
