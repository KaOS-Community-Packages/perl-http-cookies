pkgname=perl-http-cookies
pkgver=6.01
pkgrel=1
pkgdesc="HTTP cookie jars"
arch=('x86_64')
url="http://search.cpan.org/dist/HTTP-Cookies"
license=('PerlArtistic' 'GPL')
depends=('perl' 'perl-http-date' 'perl-http-message')
options=('!emptydirs')
source=(http://search.cpan.org/CPAN/authors/id/G/GA/GAAS/HTTP-Cookies-$pkgver.tar.gz)
sha1sums=('a8601a34e62666572bc8a4a98f56822b008afd17')

build() {
  cd HTTP-Cookies-$pkgver
  perl Makefile.PL INSTALLDIRS=vendor
  make
}

check() {
  cd HTTP-Cookies-$pkgver
  make test
}

package() {
  cd HTTP-Cookies-$pkgver
  make DESTDIR="$pkgdir" install
}
