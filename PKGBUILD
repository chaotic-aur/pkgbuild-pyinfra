# Maintainer: Stefan Tatschner <stefan@rumpelsepp.org>

pkgname=pyinfra
pkgver=2.6
pkgrel=1
pkgdesc="pyinfra automates infrastructure super fast at massive scale"
arch=('any')
url="https://pyinfra.com/"
license=('MIT')
depends=("python" "python-gevent" "python-paramiko" "python-click" "python-colorama"
         "python-docopt" "python-jinja" "python-dateutil" "python-pywinrm" "python-configupdater")
makedepends=('python-setuptools')
source=("https://github.com/Fizzadar/pyinfra/archive/v$pkgver.tar.gz")
sha256sums=('fe0d0fcd8f6a92ed2862c7a32a515ba817ff121380139e58524122fb0a0325bd')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  python3 setup.py build
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  python3 setup.py install --root="$pkgdir/" --optimize=1 --skip-build
}

