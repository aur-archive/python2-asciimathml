# Maintainer: Dennis Fink <the_metalgamer@hackerspace.lu>

pkgname=python2-asciimathml
pkgver=0.9.4.1
pkgrel=3
pkgdesc="ASCIIMathML to MathML translator"
arch=('any')
url="http://pypi.python.org/pypi/asciimathml/"
license=('GPL')
depends=('python2')
source=("http://pypi.python.org/packages/source/a/asciimathml/asciimathml-${pkgver}.tar.gz")
md5sums=('ab799ab8cd3d607060302f8fd3acae8f')

build() {

  cd "$srcdir/asciimathml-$pkgver"
  python2 setup.py build

}

package() {

  cd "$srcdir/asciimathml-$pkgver"

  python2 setup.py install --root=$pkgdir --optimize=1
  install -D -m644 $srcdir/asciimathml-$pkgver/COPYING "${pkgdir}"/usr/share/licenses/"${pkgname}"/LICENSE

}

# vim:set ts=2 sw=2 et:
