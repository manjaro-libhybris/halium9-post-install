# Maintainer: Bardia Moshiri <fakeshell@bardia.tech>

pkgname=halium9-post-install
pkgver=21$(date +%y%m%d)
pkgrel=3
pkgdesc="Manjaro libhybris Halium 9 post install script"
arch=('any')
url="https://github.com/manjaro-libhybris/halium9-post-install"
license=('GPL')
depends=('gzip' 'glibc-locales' 'wget' 'systemd')
source=("halium9-post-install"
        "halium9-post-install.service"
        "android.conf"
        "90_manjaro.gschema.override")
install=$pkgname.install
sha256sums=('e5bc39ff45ad1d29cfa389bc1417df2625e5cd28a863cc45a8db701dc1d96943'
            'd1cfdc5b3c7407d754c74997e46ba2b57e2c69ef1ae26b62eac6abfebc756889'
            '5571610e4cee293e8776b33ec225ca24af05197cfd7c3ebd3c2e8d830efd55b0'
            '6f4e716d6e3585cb60b21c64ea75eebdc537238e5a5a065c21ae4ac05e7c3a53')

package() {
    install -Dm755 "${srcdir}/halium9-post-install" -t "${pkgdir}/usr/bin/"
    install -Dm644 "${srcdir}/halium9-post-install.service" -t "${pkgdir}/usr/lib/systemd/system/"
    install -Dm644 "${srcdir}/android.conf" -t "${pkgdir}/usr/lib/sysusers.d/"
    install -Dm644 "${srcdir}/90_manjaro.gschema.override" -t "${pkgdir}/usr/share/glib-2.0/schemas/"
}
