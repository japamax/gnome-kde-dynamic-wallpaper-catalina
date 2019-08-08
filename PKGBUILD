# Maintainer: Christophe LAVIE <christophe.lavie@laposte.net>

pkgbase='catalina-wallpaper'
pkgname=("${pkgbase}-timed-gnome" "${pkgbase}-kde" )
_gitname='gnome-kde-catalina-dynamic-wallpaper'
pkgver=1.0.r5.g0f509cb
pkgrel=1
arch=('any')
url="https://github.com/japamax/${_gitname}"
source=("git+https://github.com/japamax/${_gitname}")
sha256sums=('SKIP')

pkgver() {
  cd $_gitname
  git describe --tags --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
}

build(){
	cd "${srcdir}/${_gitname}"
	install -dm755 "${pkgdir}/usr/share/dynamicwallpapers/catalina/Images"
	install -m644 ${srcdir}/${_gitname}/catalina/* "${pkgdir}/usr/share/dynamicwallpapers/catalina/Images"
}

 package_catalina-wallpaper-timed-gnome() {
	depends=(gnome-shell gnome-backgrounds)
	pkgdesc="GNOME time based Catalina wallpaper with real scheludes"
	ln -s "${pkgdir}/usr/share/dynamicwallpapers/catalina/Images" "${pkgdir}/usr/share/backgrounds/gnome/catalina"
	install -Dm644 catalina-timed.xml "${pkgdir}/usr/share/backgrounds/gnome/catalina-timed.xml"
	install -Dm644 catalina.xml "${pkgdir}/usr/share/gnome-background-properties/catalina.xml"
 }
 
 package_catalina-wallpaper-kde() {
	depends=(plasma5-wallpapers-dynamic)
	pkgdesc="KDE Azimuth Elevation based Catalina wallpaper"
	cd "${srcdir}/${_gitname}"
	install -Dm644 catalina.json "${pkgdir}/usr/share/dynamicwallpapers/catalina/metadata.json"
 }
 
 
