pkgname=tcgmail-git
_gitname=tcgmail
pkgver=1.0.23.g6a3a26c
pkgrel=1
pkgdesc="A  text-based notifier for gmail"
arch=('any')
url="http://github.com/cdede/tcgmail/"
license=('GPL3')
depends=('python2')
makedepends=('git' )

source=('git+https://github.com/cdede/tcgmail.git')
sha256sums=('SKIP')

pkgver() {
  cd $_gitname
  git describe --always | sed 's|-|.|g'
}

build() {
  cd $_gitname
  python2 setup.py build
}

package() {
  cd $_gitname
  python2 setup.py install --root="$pkgdir/" --optimize=1
}
