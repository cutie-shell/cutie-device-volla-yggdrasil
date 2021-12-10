
## $Id$
# Maintainer: CErik Inkinen <erik.inkinen@gmail.com>

_host="github.com"
_project=manjaro-libhybris
_basename=nemo-device-yggdrasil
_branch=master

_gitname=$_basename
pkgname=nemo-device-yggdrasil

pkgver=0.8
pkgrel=1
pkgdesc="Volla Phone specific files for GlacierUX"
arch=('aarch64')
url="https://$_host/$_project/$_gitname#branch=$_branch"
license=('BSD-3-Clause')
depends=()

makedepends=('git')
provides=("${pkgname%-git}")
conflicts=("${pkgname%-git}")
source=("${pkgname}::git+${url}")
sha256sums=('SKIP')

package() {
    mkdir -p ${pkgdir}

    cp -r ${srcdir}/nemo-device-yggdrasil/sparse/* ${pkgdir}/
    sed -r "s/NEMOVER/${pkgver}/" ${srcdir}/nemo-device-yggdrasil/sparse/etc/hw-release > ${pkgdir}/etc/hw-release
}
