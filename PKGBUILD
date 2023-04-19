pkgname='blend-inst-git'
pkgver=r3.76d89ef
pkgrel=1
pkgdesc='blendOS Installer Framework'
arch=(any)
depends=('squashfs-tools')
provides=('blend-inst')
conflicts=('blend-inst')
source=('git-inst::git+https://github.com/blend-os/blend-inst.git')
sha256sums=('SKIP')

pkgver() {
    cd "${srcdir}/git-inst"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd "${srcdir}/git-inst"
    install -Dm755 blend-inst -t "${pkgdir}/usr/bin/"
}
