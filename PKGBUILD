# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-test-distmanifest'
pkgver='1.012'
pkgrel='1'
pkgdesc="Author test that validates a package MANIFEST"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-module-manifest>=0.07')
makedepends=('perl-test-nowarnings>=0.084')
url='http://search.cpan.org/dist/Test-DistManifest'
source=('http://search.cpan.org/CPAN/authors/id/E/ET/ETHER/Test-DistManifest-1.012.tar.gz')
md5sums=('6beebac10308f7164c78eca13fd8d1b8')
sha512sums=('5cb4de5808a451ae927466fd0cd8127cba22e3fa80862070499733ef504bfe9418b10d76e83a75e1908c74ad5efb7ef3f17c8432dd3505c394520aaba03646a9')
_distdir="Test-DistManifest-1.012"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
