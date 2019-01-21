# Maintainer: Hugo Barrera <hugo@barrera.io>
# Contributor: liberodark

pkgname=tusk
pkgver=0.21.0
pkgrel=0
pkgdesc="Refined Evernote desktop app"
arch=('x86_64')
url="https://github.com/klaussinani/tusk"
license=('MIT')
depends=('xdg-utils')
source=("https://github.com/klaussinani/tusk/releases/download/v${pkgver}/tusk_${pkgver}_amd64.deb"
        $pkgname.desktop
        $pkgname.png)
sha512sums=('82ec2dd1e6e889d847cc0f8f9e8886b8fd999a54fb1f827c78bc6b9ff50aecf7bde47290915704edfc100b7c857b79633f6285e7a6cfa13715c2767f91baf3d8'
            'caef9e0da72e70bb8d393f16d98098f6586530a278fade4d6d15b81820f4d5435c4c7ef2255fcc1815ce6681aeca55411235922a6f817451f8f63ecd191ac35c'
            '46afc3aad7d1a518df8abcebe75d7576c9fda3a10f8b046d9e7399ce76e2035e0c1db5abbedc62ff259d10c16630062d74dca93d42f1c3b5b9787146393b76f4')

package() {
  cd $srcdir
  tar xvf data.tar.xz
  cp -r opt $pkgdir
  install -vDm644 $srcdir/$pkgname.desktop $pkgdir/usr/share/applications/$pkgname.desktop
  install -vDm644 $srcdir/$pkgname.png $pkgdir/usr/share/pixmaps/$pkgname.png

  mkdir -p "$pkgdir/usr/bin/"
  ln -sf "/opt/Tusk/tusk-app" "$pkgdir/usr/bin/tusk-app"
}
