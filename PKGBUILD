# Maintainer: Erik Inkinen <erik.inkinen@gmail.com>

pkgname=halium9-post-install
pkgver=20$(date +%y%m%d)
pkgrel=4
pkgdesc="Manjaro ARM's Halium 9 post install script"
arch=('any')
url="https://www.manjaro.org"
license=('GPL')
depends=('gzip' 'glibc-locales' 'wget' 'systemd')
source=("halium9-post-install"
        "halium9-post-install.service"
        "android.conf"
        "lomiri-gtk.css"
        "ril_subscription.conf"
        "90_manjaro.gschema.override")
install=$pkgname.install
md5sums=('6d4f36fc915ea8cb3acd9179e4bca14c'
         '61fd3d0e518f087210f56e2b0acf923b'
         'a3447f23611d71f9d68515b09527c721'
         '697420d8cfb1acb3a6b55a364a267f24'
         '23c0519d2ee8531009611d9f7bd47353'
         'bd274d0019ac5b378aec92ecd823d75a')

package() {
    install -Dm755 "${srcdir}/halium9-post-install" -t "${pkgdir}/usr/bin/"
    install -Dm644 "${srcdir}/halium9-post-install.service" -t "${pkgdir}/usr/lib/systemd/system/"
    install -Dm644 "${srcdir}/android.conf" -t "${pkgdir}/usr/lib/sysusers.d/"
    install -Dm644 "${srcdir}/lomiri-gtk.css" "${pkgdir}/opt/halium9-post-install/lomiri/gtk.css"
    install -Dm644 "${srcdir}/ril_subscription.conf" "${pkgdir}/etc/ofono/ril_subscription.conf"
    install -Dm644 "${srcdir}/90_manjaro.gschema.override" -t "${pkgdir}/usr/share/glib-2.0/schemas/"
}
