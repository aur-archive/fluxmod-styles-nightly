# Contributor: Joel Almeida <aullidolunar at gmail dot c0m>

pkgname=fluxmod-styles-nightly
pkgver=1
pkgrel=3
pkgdesc="Nightly tarball of all styles for fluxbox from http://tenr.de/styles/"
arch=('any')
url="http://tenr.de/styles/"
license=('CC BY-SA 3.0')
depends=('fluxbox')
source=("http://tenr.de/styles/archives/tenr.de-styles-pkg.tar.bz2")
md5sums=('78dc07262c72c876fc80b9710a4d4009')

build() {
	cd "$srcdir"
}

package() {
	cd "$srcdir/tenr.de-styles-pkg"
	install -dm755 "$pkgdir/usr/share/fluxbox/styles"
	install -Dm644 License "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
	rm License
	# selected themes are installed by default in fluxbox, remove them
	rm -rf arch bora_green bora_blue bloe bora_black bora_black carp green_tea ostrich zimek_bisque zimek_darkblue zimek_green
	find . -type f -exec install -Dm644 '{}' "$pkgdir/usr/share/fluxbox/styles/{}" \;
}
