# Maintainer: Justin C Miller <justin@justin.cm>
pkgname=foundryvtt
pkgver=12.331
pkgrel=1
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
	FoundryVTT-$pkgver.zip
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
	cp -r "$srcdir"/locales "$srcdir"/resources "$pkgdir"/usr/lib/foundryvtt/
	chown -R $pkdusers:$pkggroups "$pkgdir"/usr/lib/foundryvtt
}

sha512sums="
a17947511c1877e904496d8fbe7ca946ecf83f0c4b88af99eb43cb12533790265308b92e2ca477abd56077e9a904d08ea4e01d675cab9c7694cfd3fac56a572e  foundryvtt.initd
757024ff6f58afb03faffcf123f78bc1e5a945b387c1b2061c684662077e1b56e2ce77d09200253b42552e03ee29f46bfab4efa727b78992278d8be1feb8c299  foundryvtt.confd
e5b306732379d5471437356c5692d125d07891a579292528c661b34d485cc844b04a774779a130997ed83629b96e124d9d017784d2cf8b2ce12b80bfe5e0a2c3  FoundryVTT-12.331.zip
"
