# Maintainer: Chris Fordham <chris at fordham-nagy dot id dot au> aka flaccid
# Contributor: Ferrazzo Riccardo <f.riccardo87@gmail.com>
# Package Source: https://github.com/flaccid/archlinux-packages/blob/master/qtjambi-beta/PKGBUILD

pkgname=qtjambi-beta
_pkgname=qtjambi
pkgver=4.7.0beta2
_pkgver=4.7.0-beta2
_version=4.7.0
pkgrel=2
arch=('i686' 'x86_64')
pkgdesc="The Qt library made available to Java."
url="http://qt-jambi.org/"
license=('GPL')
depends=('java-environment-common' 'libpng')
conflicts=('qtjambi')
replaces=('qtjambi')

_os='linux'
_arch='32'
[ ${CARCH} = 'x86_64' ] && _arch='64'

source=("http://downloads.sourceforge.net/${_pkgname}/${_pkgname}-${_os}${_arch}-community-${_pkgver}.tar.gz")
sha1sums=('d8120e104c7fa041fdb0310c7167ff15127a621d')
[ ${CARCH} = "x86_64" ] && sha1sums[0]='d8120e104c7fa041fdb0310c7167ff15127a621d'

package() {
  install -d "${pkgdir}/opt/${pkgname}"
  cp -ar "${_pkgname}-${_os}${_arch}-community-${_version}" "${pkgdir}/opt/${pkgname}"

  install -d "${pkgdir}/usr/share/java/${pkgname}"
  for j in *.jar; do
    ln -s "${pkgdir}/usr/share/java/${pkgname}/$j" "${pkgdir}/usr/share/java/${pkgname}"
  done
}
