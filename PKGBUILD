# Maintainer: agnotek <agnostic.sn [at] gmail [dot] com>

pkgname=ytplmp3
pkgver=5.0
pkgrel=2
pkgdesc="YTPLMP3 - only german version"
arch=('any')
url="http://youtube.com/"
license=('GPL3')
makedepends=('zip')
options=('!strip')
install="ytplmp3.install"
md5sums=('SKIP'
         '8ab48196af3d5a15dba233fa8b49e784'
         '267dc97a7ed70840d928d4170087a5a1')

source=("https://dl.dropboxusercontent.com/u/9839330/YTPLMP3/YTPLMP3-${pkgver}.tar.gz"
        "ytplmp3.install"
        "ytplmp3.desktop")

package() {
  cd "${srcdir}"

  install -dm755 "${pkgdir}/usr/share/${pkgname}"
  install -dm755 "${pkgdir}/usr/bin"

  # Program
  echo "${pkgdir}/usr/share/${pkgname}/"
  install -Dm755 ${srcdir}/YTPLMP3 "${pkgdir}/usr/share/${pkgname}/"

  # Link to program
  mkdir -p "${pkgdir}/usr/bin"
  ln -s "/usr/share/${pkgname}/YTPLMP3" "${pkgdir}/usr/bin/YTPLMP3"

  # Desktop file
  install -Dm644 "${srcdir}/ytplmp3.desktop" "${pkgdir}/usr/share/applications/ytplmp3.desktop"

}
