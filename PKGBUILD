# Maintainer: Erik Inkinen <erik.inkinen@gmail.com>

pkgname=halium9-post-install
pkgver=20$(date +%y%m%d)
pkgrel=2
pkgdesc="Manjaro ARM's Halium 9 post install script"
arch=('any')
url="https://www.manjaro.org"
license=('GPL')
depends=('gzip' 'glibc-locales')
source=("halium9-post-install"
        "halium9-post-install.service"
        "android.conf"
        "lomiri-gtk.css")
install=$pkgname.install
md5sums=('269b102d6f844bec50abcc8be32628c0'
         '61fd3d0e518f087210f56e2b0acf923b'
         'a3447f23611d71f9d68515b09527c721'
         '697420d8cfb1acb3a6b55a364a267f24')

package() {
    install -Dm755 "${srcdir}/halium9-post-install" -t "${pkgdir}/usr/bin/"
    install -Dm644 "${srcdir}/halium9-post-install.service" -t "${pkgdir}/usr/lib/systemd/system/"
    install -Dm644 "${srcdir}/android.conf" -t "${pkgdir}/usr/lib/sysusers.d/"
    install -Dm644 "${srcdir}/lomiri-gtk.css" "${pkgdir}/opt/pinephone-post-install/lomiri/gtk.css"
}
