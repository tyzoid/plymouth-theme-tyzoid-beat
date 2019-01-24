# Maintainer: Nenad Stojanovikj <nekk1@live.com>

pkgname=plymouth-theme-tyzoid-beat
pkgver='0.1'
pkgrel=1
pkgdesc='Plymouth theme with pulsating tyzoid logo.'
arch=('any')
license=('MIT')
depends=('plymouth')

package() {
  cd "tyzoid-beat"

  _themedir="$pkgdir/usr/share/plymouth/themes/tyzoid-beat"

  for N in *.png tyzoid-beat.plymouth tyzoid-beat.script; do
    install -Dm644 $N "${_themedir}/$N"
  done

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -Dm644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
}

post_install() {
	echo "To install the theme run:"
	echo "sudo plymouth-set-default-theme -R tyzoid-beat"
}
