# Maintainer: Christian Weber <ChristianWeber802 at gmx dot net>

pkgname=notificathor
pkgver=0.5.0
pkgrel=2
pkgdesc="Themeable On Screen Displays for X"
arch=('i686' 'x86_64')
url="https://github.com/TheWebster/NotificaThor/"
license=('custom:BSD')
depends=('cairo>=1.12.0')
makedepends=('gcc' 'make' 'libxcb' 'cairo>=1.12.0' 'freetype2')
optdepends=('xbindkeys: show OSDs on keypress')
backup=('etc/NotificaThor/rc.conf' 'etc/NotificaThor/themes/onyx-citrus'\
        'etc/NotificaThor/themes/simple' 'etc/NotificaThor/themes/slim'\
        'etc/NotificaThor/themes/bloody-concrete')
source=("https://github.com/TheWebster/NotificaThor/archive/v$pkgver.tar.gz")
md5sums=('96abf0d4542ea3a1745fbde03ee8a435')


build() {
	cd "$srcdir/NotificaThor-$pkgver"
	make
}

package() {
	cd "$srcdir/NotificaThor-$pkgver"
	mkdir -p "$pkgdir/usr/bin" "$pkgdir/usr/share/man" "$pkgdir/etc" \
	         "$pkgdir/usr/share/licenses/$pkgname"
	cp LICENCE.md $pkgdir/usr/share/licenses/$pkgname/LICENSE
	make prefix="$pkgdir" install
}
