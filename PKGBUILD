# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=conductor
pkgname=ruby-$_gemname
pkgver=0.9.4
pkgrel=2
pkgdesc='lets you just try things while always maximizing towards a goal (e.g. purchase, signups, etc)'
arch=(any)
url='https://github.com/rails/conductor'
license=(MIT)
depends=(ruby ruby-rails-3 ruby-googlecharts ruby-haml)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('c1629a05d97bcda4d0f53a098b46e44a47349a92')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/MIT-LICENSE" "$pkgdir/usr/share/licenses/$pkgname/MIT-LICENSE"
}
