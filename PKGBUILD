# Maintainer: Sea Zones <seazones@163.com>
pkgname=go-ceph-lib
pkgver=12.2.13
pkgrel=1
pkgdesc="the old version(luminous) ceph-${pkgver} devel libraries for go-ceph"
arch=("x86_64")
url="https://github.com/ceph/go-ceph"
license=("LPGP-2.1 LGPL-3")
_mirror="https://mirrors.ustc.edu.cn/"
_mirror_url="${_mirror}ceph/rpm-luminous/el7/x86_64/"
groups=()
depends=()
makedepends=("rpmextract")
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(
	"${_mirror_url}librados-devel-${pkgver}-0.el7.x86_64.rpm"
	"${_mirror_url}librbd-devel-${pkgver}-0.el7.x86_64.rpm"
	"${_mirror_url}libcephfs-devel-${pkgver}-0.el7.x86_64.rpm"
)
noextract=()
prepare() {
  mkdir ${pkgname}-${pkgver}
  cd ${pkgname}-${pkgver}
  rpmextract.sh  "../librados-devel-${pkgver}-0.el7.x86_64.rpm" "../librbd-devel-${pkgver}-0.el7.x86_64.rpm" "../libcephfs-devel-${pkgver}-0.el7.x86_64.rpm"
}

package() {
  cd "$pkgname-$pkgver"
  cp -r ./ ${pkgdir}/
}
sha256sums=('02b4d0e64c9b9115c993fa491cac3fc4ddfa17a4287eb2b8d19ffbb923c435af'
            'c59e65f96a9a4119242db85e5773802162d55bae6c86ceec854da4829edae88a'
            '1bfda2b3f837e189ed777fd4dc6d7909794f720a485a32f61f0ff6c8487f220c')
