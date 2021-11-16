_realname='git-credential-manager-core'
pkgname="${_realname}-bin"
pkgver=2.0.603
_buildver=10294
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/microsoft/Git-Credential-Manager-Core'
license=('MIT')
source=("https://github.com/microsoft/Git-Credential-Manager-Core/releases/download/v${pkgver}/gcmcore-win-x86-${pkgver}.${_buildver}.zip")
depends=('git')
conflicts=('git-credential-manager-bin')
install="${pkgname}.install"
sha256sums=('b9326f367b34e1023252978b64d05ef9fa73241ec4a4949fe5b9c3e0a01416a1')

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
