# Contributor: waffenladen <holger at music-nerds.net>
# Contributor: Bernardo Barros <bernardobarros@gmail.com>
# Contributor: missingsense <rbeenen@gmail.com>

pkgname=pd-gem
_pkgname=Gem
pkgver=0.93.3
pkgrel=1
pkgdesc="Graphics Environment for Multimedia - an external for PureData"
arch=('i686' 'x86_64')
url="http://puredata.info/community/projects/software/gem"
depends=('pd' 'libgl' 'libtiff' 'libjpeg' 'ftgl' 'mesa' 'avifile')
license=('GPL2')
source=(http://puredata.info/community/projects/software/gem/releases/$pkgver/$_pkgname-$pkgver.tar.gz)
md5sums=('06ec538d157b06cbb2972c0e137ddb48')


build() {

  cd ${startdir}/src/${_pkgname}-${pkgver}
  autoconf
  ./configure --prefix=/usr --without-ffmpeg
  make
  make DESTDIR=$startdir/pkg install
  chmod a+x $startdir/pkg/usr/lib/pd/extra/Gem/examples{,/*}
  chmod a+r -R $startdir/pkg/usr/lib/pd/extra/Gem/examples
}
