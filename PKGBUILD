# Maintainer: Dr.Schliemann <doktor.schliemann at gmail dot com>
# Contributor: JHeaton <jheaton at archlinux dot us>

pkgname=basenji
pkgver=1.0.1
pkgrel=1
pkgdesc="Volume indexing tool designed for easy and fast indexing of CD/DVD and other type of volume collections."
arch=('i686' 'x86_64')
url="https://launchpad.net/basenji"
license=('GPL')
depends=('mono>=2.4' 'gtk-sharp-2>=2.12.9' 'gnome-desktop2>=2.32.0'
	 'gio-sharp>=0.3' 'dbus-sharp>=0.7.0' 'dbus-sharp-glib>=0.5'
	 'taglib-sharp>=2.0.4.0' 'udisks>=1.0.1')
source=(https://launchpad.net/basenji/trunk/$pkgver/+download/$pkgname-$pkgver.tar.gz)
md5sums=('eee951ac995359bedab23b964a8e5502')

build() {
  cd "$srcdir/"

  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/"

  make DESTDIR="$pkgdir/" install
}
