# Maintainer: Bardia Moshiri <fakeshell@bardia.tech>

pkgname=halium9-post-install
pkgver=21$(date +%y%m%d)
pkgrel=2
pkgdesc="Manjaro libhybris Halium 9 post install script"
arch=('any')
url="https://github.com/manjaro-libhybris/halium9-post-install"
license=('GPL')
depends=('gzip' 'glibc-locales' 'wget' 'systemd')
source=("halium9-post-install"
        "halium9-post-install.service"
        "android.conf"
        "ril_subscription.conf"
        "90_manjaro.gschema.override")
install=$pkgname.install
sha256sums=('00c0d3e0692dda3b7a26618613a3d6b4d04ee31b4bfd848d2686ff51d03d74d9'
            'd1cfdc5b3c7407d754c74997e46ba2b57e2c69ef1ae26b62eac6abfebc756889'
            '5571610e4cee293e8776b33ec225ca24af05197cfd7c3ebd3c2e8d830efd55b0'
            'f032810ea128d4cf9377d144cded32cbf1a2ed18087403fe706a1f9707fd0d7f'
            '18d06f03830a8afa75a774d61c4b9ec4fca9b8d3594bb3e19e6d38f3a652fbdb')

package() {
    install -Dm755 "${srcdir}/halium9-post-install" -t "${pkgdir}/usr/bin/"
    install -Dm644 "${srcdir}/halium9-post-install.service" -t "${pkgdir}/usr/lib/systemd/system/"
    install -Dm644 "${srcdir}/android.conf" -t "${pkgdir}/usr/lib/sysusers.d/"
    install -Dm644 "${srcdir}/ril_subscription.conf" "${pkgdir}/etc/ofono/ril_subscription.conf"
    install -Dm644 "${srcdir}/90_manjaro.gschema.override" -t "${pkgdir}/usr/share/glib-2.0/schemas/"
}
