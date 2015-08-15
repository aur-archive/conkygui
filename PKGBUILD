# Contributor: Forrest Page
# Maintainer: Meya <meya at posteo dot se>

pkgname=conkygui
pkgdesc="A graphical configuration tool for Conky written in Java."
pkgver=1.3.1
pkgrel=2
arch=('i686' 'x86_64')
url="http://conkygui.sourceforge.net/"
license=('GPL')
depends=('jre7-openjdk' 'scala')
makedepends=('imagemagick' 'unzip' 'tar')
source=(http://sourceforge.net/projects/conkygui/files/tarbz2/conkyguiv1.3.1%28scala-2.8.0%29.tar.bz2/download)
md5sums=('50745ec7ada7109c9a00f3e486c60474')

build() {
    cd ${srcdir}/conkyguiv1.3.1/
    
    # copy libs
    mkdir -p ${pkgdir}/usr/share/applications ${pkgdir}/usr/bin ${pkgdir}/usr/share/man/man1/ \
    	     ${pkgdir}/usr/share/pixmaps ${pkgdir}/usr/share/doc/conkygui/ \
	     ${pkgdir}/usr/share/conkygui/lib/

    cp -v ./lib/* ${pkgdir}/usr/share/conkygui/lib
    cp -v ./conkygui.jar ${pkgdir}/usr/share/conkygui
    # copy to bin
    cp -v ./conkygui ${pkgdir}/usr/bin
    cp -v ./conkygui-remove ${pkgdir}/usr/bin
    # copy icon image
    cp -v ./conkygui.png ${pkgdir}/usr/share/pixmaps
    # copy desktop file
    cp -v ./conkygui.desktop ${pkgdir}/usr/share/applications
    # copy man page
    cp -v ./man/conkygui.1.gz ${pkgdir}/usr/share/man/man1/
    # copy docs
    cp -v ./doc/* ${pkgdir}/usr/share/doc/conkygui/
}
