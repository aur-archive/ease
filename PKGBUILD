# Maintainer: ninian <mcfadzean.org.uk ta linux>

pkgname=ease
pkgver=1.6.1
pkgrel=1
pkgdesc="Opens files and URLs with applications associated by name or mimetype; an xdg-open replacement for control freaks. Applications and associations may be customized using an SQLite database."
arch=('any')
url="http://appstogo.mcfadzean.org.uk/linux.html#ease"
license=('custom:MPL2')
depends=('bash' 'dmenu' 'sqlite' 'libnotify' 'file')
optdepends=('perl-file-mimeinfo: to better determine mimetypes' 'sqlitebrowser: to manage database' 'sudo: to run applications as root' 'gxmessage: to view .desktop files')
source=("http://appstogo.mcfadzean.org.uk/dl/$pkgname/$pkgname-$pkgver.tar.gz")
md5sums=('be1eeb143f28b12ddc7300cfd84b7f14')

package() {
  cd "$srcdir/${pkgname}-$pkgver"
  install -Dm755 ${pkgname}                  "$pkgdir/usr/bin/${pkgname}"
  install -Dm644 ${pkgname}.png              "$pkgdir/usr/share/pixmaps/${pkgname}.png"
  install -Dm644 ${pkgname}.desktop          "$pkgdir/usr/share/applications/${pkgname}.desktop"
  install -Dm644 ${pkgname}.conf             "$pkgdir/usr/share/doc/${pkgname}/${pkgname}.conf"
  install -Dm644 ${pkgname}_example.sqlite   "$pkgdir/usr/share/doc/${pkgname}/${pkgname}_example.sqlite"
  install -Dm644 LICENSE                     "$pkgdir/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 README                      "$pkgdir/usr/share/doc/${pkgname}/README"
  install -Dm644 CHANGELOG                   "$pkgdir/usr/share/doc/${pkgname}/CHANGELOG"
  install -Dm755 dudo                        "$pkgdir/usr/share/doc/${pkgname}/dudo"
  install -Dm755 xdg-open                    "$pkgdir/usr/share/doc/${pkgname}/xdg-open"
  msg "Copy sample configuration file /usr/share/doc/${pkgname}/${pkgname}.conf and customize per user"
  msg "Also see 'ease -h' and /usr/share/doc/${pkgname}/README for more information"
  msg ">>>> Database format changed in versions >= 1.60 - see /usr/share/doc/ease/CHANGELOG <<<<"
}
