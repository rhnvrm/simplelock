# Maintainer: Rohan Verma <hello@rohanverma.net>
pkgname='simplelock'
pkgver='v0.0.1'
pkgrel=1
pkgdesc="Fast and simple wrapper over i3lock with multiple modes. Supports xkcd and unsplash"
arch=('any')
url=""
license=('MIT')
groups=()
depends=('i3lock')
makedepends=()
checkdepends=()
optdepends=()
provides=('simplelock')
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=('simplelock' 'lock.png' 'lockscreen.png') 
noextract=()
md5sums=('b3fd1ab5840cf0c2cbbc055d14c2bc9c'
         '20745271b749810575648ebcd4844716'
         '3df461bfa1643b4f20aa8701d3e91f61')
validpgpkeys=()

package() {
	mkdir -p ~/.config/simplelock
	cp $srcdir/lock.png ~/.config/simplelock/
	cp $srcdir/lockscreen.png ~/.config/simplelock/
	install -D -t "$pkgdir/usr/bin" "$srcdir/simplelock"
}
