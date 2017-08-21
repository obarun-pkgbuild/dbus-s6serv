# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dbus-s6serv
pkgver=0.1
pkgrel=6
pkgdesc="dbus service for s6"
arch=(x86_64)
license=('beerware')
depends=('dbus' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('dbus.daemon.finish.s6'
		'dbus.daemon.run.s6'
		'dbus.log.run.s6'
		'dbus.logd'
		'LICENSE')
md5sums=('0963f8a3678d1e6d509e2ef38f5ecfa3'
         '874be4284f7c5dc07b1641c331fa2e9d'
         'cb00245c0890acb120900c9d32a3955e'
         '64e305bd0dd8d1008abfcd67b9817651'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/dbus.daemon.finish.s6" "$pkgdir/etc/s6-serv/available/classic/dbus/finish"
	install -Dm 0755 "$srcdir/dbus.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/dbus/run"
	
	# log
	install -Dm 0755 "$srcdir/dbus.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/dbus/log/run"
	install -Dm 0644 "$srcdir/dbus.logd" "$pkgdir/etc/s6-serv/log.d/dbus"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dbus-s6serv/LICENSE"
}
