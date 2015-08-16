# Maintainer: Joffrey TISSERON <tisseron.joffrey@aliceadsl.fr>

_name=image2pdf
pkgname="kdeservicemenu-$_name"
_number=118537
pkgver=0.9
pkgrel=1
pkgdesc=' Servicemnu to convert images to pdfs.'
arch=('i686' 'x86_64')
url="http://kde-apps.org/content/show.php/$_name?content=$_number"
license=('GPL')
depends=('kdelibs' 'imagemagick')
conflicts=("$_name-servicemenu-kde4")
replaces=("$_name-servicemenu-kde4")
source=("http://kde-apps.org/CONTENT/content-files/$_number-$_name.desktop"
	'image2pdf.patch')
md5sums=('2a9e65af8f1a3d80541bcfa6de6d6bc9'
	 'bdc202d611762785832638a24c3f9625')

build() {
  cd $srcdir
  patch $_number-$_name.desktop image2pdf.patch
}

package() {
   mkdir -p "$pkgdir/$(kde4-config --prefix)/share/kde4/services/ServiceMenus"
   cp $srcdir/$_number-$_name.desktop "$pkgdir/$(kde4-config --prefix)/share/kde4/services/ServiceMenus/$_name.desktop"
   chmod 644 "$pkgdir/$(kde4-config --prefix)/share/kde4/services/ServiceMenus/$_name.desktop"
}