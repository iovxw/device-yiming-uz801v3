# Reference: <https://postmarketos.org/devicepkg>
pkgname=device-yiming-uz801v3
pkgdesc="Yiming uz801 v3.0 4G Modem Stick"
pkgver=0.1
pkgrel=0
url="https://postmarketos.org"
license="MIT"
arch="aarch64"
options="!check !archcheck"
depends="postmarketos-base mkbootimg linux-postmarketos-qcom-msm8916
	 soc-qcom-msm8916 soc-qcom-msm8916-rproc
"
makedepends="devicepkg-dev"
source="deviceinfo"
subpackages="$pkgname-nonfree-firmware:nonfree_firmware"
_pmb_select="soc-qcom-msm8916-rproc"

build() {
	devicepkg_build $startdir $pkgname
}

package() {
	devicepkg_package $startdir $pkgname
}

nonfree_firmware() {
	pkgdesc="GPU/WiFi/BT/Modem/Video firmware"
	depends="firmware-qcom-adreno-a300 msm-firmware-loader
		 firmware-qcom-msm8916-wcnss firmware-huawei-y635-wcnss-nv
		 firmware-qcom-msm8916-venus"
	mkdir "$subpkgdir"
}

sha512sums="
21e3840490fda230c8d0f9f4e154221f7d944f730bfb78f82ec669d9bcf7f4dd4282b8cb15f199c6278f74376ae311d682c72a755b72759253446a38cd77adae  deviceinfo
"
