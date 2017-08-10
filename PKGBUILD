# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=cups-s6serv
pkgver=0.1
pkgrel=2
pkgdesc="cups service for s6"
arch=(x86_64)
license=('beerware')
depends=('cups' 's6' 's6-rc' 's6-boot')
conflicts=()
install=cups-s6serv.install
source=('cups.daemon.run.s6'	
		'cups.log.run.s6'
		'LICENSE')
md5sums=('17ff79ab7ee6f2b0297baf12d4b99375'
         '38b0a3209f1e89133ad4acb396a47689'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/cups.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/cups/run"
	
	# log
	install -Dm 0755 "$srcdir/cups.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/cups/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/cups-s6serv/LICENSE"
}
