# Maintainer: Christophe LAVIE <christophe.lavie@laposte.net>

pkgbase='dynamic-wallpaper-catalina'
pkgname=("${pkgbase}-timed-gnome" "${pkgbase}-kde" "${pkgbase}-images" )
_gitname='gnome-kde-dynamic-wallpaper-catalina'
pkgver=1.0r17.r0.ga3ebc35
pkgrel=1
install=gnome-kde-dynamic-wallpaper-catalina.install
arch=('any')
url="https://github.com/japamax/${_gitname}"
source=("git+https://github.com/japamax/${_gitname}")
sha256sums=('SKIP')

pkgver() {
  cd $_gitname
  git describe --tags --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
}

 package_dynamic-wallpaper-catalina-images() {
	cd "${srcdir}/${_gitname}"
	install -dm755 "${pkgdir}/usr/share/dynamicwallpapers/catalina/images"
	install -m644 ${srcdir}/${_gitname}/catalina/* "${pkgdir}/usr/share/dynamicwallpapers/catalina/images"
}

 package_dynamic-wallpaper-catalina-timed-gnome() {
	depends=(gnome-shell gnome-backgrounds dynamic-wallpaper-catalina-images)
	pkgdesc="GNOME time based Catalina wallpaper with real scheludes"
	cd "${srcdir}/${_gitname}"
	install -dm755 "${pkgdir}/usr/share/backgrounds/gnome"
	ln -s "/usr/share/dynamicwallpapers/catalina/images" "${pkgdir}/usr/share/backgrounds/gnome/catalina"
	install -Dm644 catalina-timed.xml "${pkgdir}/usr/share/backgrounds/gnome/catalina-timed.xml"
	install -Dm644 catalina.xml "${pkgdir}/usr/share/gnome-background-properties/catalina.xml"
 }
 
 package_dynamic-wallpaper-catalina-kde() {
	depends=(plasma5-wallpapers-dynamic dynamic-wallpaper-catalina-images)
	pkgdesc="KDE Azimuth Elevation based Catalina wallpaper"
	cd "${srcdir}/${_gitname}"
	install -Dm644 catalina.json "${pkgdir}/usr/share/dynamicwallpapers/catalina/metadata.json"
 }
 
