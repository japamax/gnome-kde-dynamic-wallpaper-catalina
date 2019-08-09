# Maintainer: Christophe LAVIE <christophe.lavie@laposte.net>

pkgbase='catalina-dynamic-wallpaper'
pkgname=("${pkgbase}-timed-gnome" "${pkgbase}-kde" "${pkgbase}-images" )
_gitname='gnome-kde-catalina-dynamic-wallpaper'
pkgver=1.0
pkgrel=6
arch=('any')
url="https://github.com/japamax/${_gitname}"
source=("git+https://github.com/japamax/${_gitname}")
sha256sums=('SKIP')

#pkgver() {
#  cd $_gitname
#  git describe --tags --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
#}

 package_catalina-dynamic-wallpaper-images() {
	cd "${srcdir}/${_gitname}"
	install -dm755 "${pkgdir}/usr/share/dynamicwallpapers/catalina/images"
	install -m644 ${srcdir}/${_gitname}/catalina/* "${pkgdir}/usr/share/dynamicwallpapers/catalina/images"
}

 package_catalina-dynamic-wallpaper-timed-gnome() {
	depends=(gnome-shell gnome-backgrounds catalina-dynamic-wallpaper-images)
	pkgdesc="GNOME time based Catalina wallpaper with real scheludes"
	cd "${srcdir}/${_gitname}"
	install -dm755 "${pkgdir}/usr/share/backgrounds/gnome"
	ln -s "${pkgdir}/usr/share/dynamicwallpapers/catalina/Images" "${pkgdir}/usr/share/backgrounds/gnome/catalina"
	install -Dm644 catalina-timed.xml "${pkgdir}/usr/share/backgrounds/gnome/catalina-timed.xml"
	install -Dm644 catalina.xml "${pkgdir}/usr/share/gnome-background-properties/catalina.xml"
 }
 
 package_catalina-dynamic-wallpaper-kde() {
	depends=(plasma5-wallpapers-dynamic catalina-dynamic-wallpaper-images)
	pkgdesc="KDE Azimuth Elevation based Catalina wallpaper"
	cd "${srcdir}/${_gitname}"
	install -Dm644 catalina.json "${pkgdir}/usr/share/dynamicwallpapers/catalina/metadata.json"
 }
 
 
