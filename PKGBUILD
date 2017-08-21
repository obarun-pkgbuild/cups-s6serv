# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=cups-s6serv
pkgver=0.1
pkgrel=4
pkgdesc="cups service for s6"
arch=(x86_64)
license=('beerware')
depends=('cups' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('cups.daemon.run.s6'	
		'cups.log.run.s6'
		'cups.logd'
		'LICENSE')
md5sums=('17ff79ab7ee6f2b0297baf12d4b99375'
         '38b0a3209f1e89133ad4acb396a47689'
         '1c012eebe0744d9837964e24a7d48b99'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/cups.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/cups/run"
	
	# log
	install -Dm 0755 "$srcdir/cups.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/cups/log/run"
	install -Dm 0644 "$srcdir/cups.logd" "$pkgdir/etc/s6-serv/log.d/cups"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/cups-s6serv/LICENSE"
}
