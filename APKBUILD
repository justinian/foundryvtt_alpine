# Maintainer: Justin C Miller <justin@justin.cm>
pkgname=foundryvtt
pkgver=13.342
pkgrel=3
pkgdesc="Foundry Virtual Tabletop"
url="https://foundryvtt.com"
arch="noarch"
options="!archcheck"
license="UNLICENSED"
depends="nodejs"
makedepends=""
checkdepends=""
install="$pkgname.pre-install"
subpackages=""
pkgusers="foundryvtt"
pkggroups="foundryvtt"
source="
	foundryvtt.initd
	foundryvtt.confd
	FoundryVTT-Node-$pkgver.zip
	"
builddir="$srcdir/"

build() {
	# Replace with proper build command(s)
	:
}

check() {
	# Replace with proper check command(s)
	:
}

package() {
	# Replace with proper package command(s)
	:
	install -m755 -D "$srcdir"/$pkgname.initd \
		"$pkgdir"/etc/init.d/$pkgname
	install -m644 -D "$srcdir"/$pkgname.confd \
		"$pkgdir"/etc/conf.d/$pkgname

	mkdir -p "$pkgdir"/usr/lib/foundryvtt
	mkdir -p "$pkgdir"/var/lib/foundryvtt
	find "$srcdir" -maxdepth 1 -type d -o -type f | xargs -I FILE cp -r FILE "$pkgdir"/usr/lib/foundryvtt/
	chown -R $pkgusers:$pkggroups "$pkgdir"/usr/lib/foundryvtt
}

sha512sums="
1660e10c373592e0ed3181d19deb156428566963da9f830bb30735e72261400748a4ef2e5c27ac3c19e880c1cae02e5b9b6edebbd625efc0b04a5b5f9667684e  foundryvtt.initd
757024ff6f58afb03faffcf123f78bc1e5a945b387c1b2061c684662077e1b56e2ce77d09200253b42552e03ee29f46bfab4efa727b78992278d8be1feb8c299  foundryvtt.confd
f0fe079a4592a4b88a6fa3e95d298a3a78aa5e7610746a52b06b59122439d4a19ba5e50cebe4201afa0ff9ca438ab3eaba1022f4ad1096f265c3fdcc2c99f258  FoundryVTT-Node-13.342.zip
"
