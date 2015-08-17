# Maintainer: Carl Mueller  archlinux at carlm e4ward com

pkgname=publictransport-library
pkgver=0.10_rc2
_pkgver=0.10-rc2
pkgrel=1
pkgdesc="Library for publictransport-plasmoid"
arch=('i686' 'x86_64')
url="http://www.kde-look.org/content/show.php/PublicTransport?content=106175"
license=('GPL')
depends=('kwebkitpart' 'kdebase-workspace')
makedepends=('git' 'cmake' 'automoc4')
options=()
build() {
  git archive --format=tar --remote=git://anongit.kde.org/publictransport unstable-$_pkgver > publictransport.tar
  cd $srcdir
  tar xf publictransport.tar
  cd libpublictransporthelper
  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` .
  make
  make DESTDIR="$pkgdir/" install
}
