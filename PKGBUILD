# Maintainer: zeteref <zeteref@gmail.com>

pkgname=gloss
pkgver=0.1.0
pkgrel=1
pkgdesc="Translate and speak text in an osd-window overlay"
arch=('any')
url="https://github.com/zeteref/gloss"
license=('MIT')
depends=('walker' 'curl' 'jq' 'mpv' 'python' 'osd-window' 'hunspell' 'hunspell-en_us' 'hunspell-pl')

# write the built package to /tmp instead of cluttering the source dir
PKGDEST=/tmp

package() {
  install -Dm755 "$startdir/gloss" "$pkgdir/usr/bin/gloss"
  install -Dm644 "$startdir/walker-theme/layout.xml" "$pkgdir/etc/xdg/walker/themes/trans/layout.xml"
  install -Dm644 "$startdir/walker-theme/style.css" "$pkgdir/etc/xdg/walker/themes/trans/style.css"
  install -Dm644 "$startdir/osd-window.toml" "$pkgdir/usr/share/gloss/osd-window.toml"
}
