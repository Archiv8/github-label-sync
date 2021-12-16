#!/bin/bash

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the 
# repository root directory, see https://github.com/koalaman/shellcheck/wiki 
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154

# Maintainer: Your Name <youremail@domain.com>
# Contributor: Your Name <youremail@domain.com>


# New variables


# Official variables
# pkgbase=""
pkgname="github-label-sync"
pkgdesc="Synchronise you GitHub labels with as few destructive operations as possible"
pkgver=2.0.2
pkgrel=1
# epoch=
url="https://github.com/Financial-Times/github-label-sync"
# license=("")
arch=("any")
# groups=()
depends=("nodejs")
makedepends=("npm")
# checkdepends=()
# optdepends=()
# provides=()
# conflicts=()
# replaces=()
# backup=()
options=("!emptydirs")
# install=
# changelog="CHANGELOG.md"
source=("https://registry.npmjs.org/$pkgname/-/$pkgname-$pkgver.tgz")
noextract=("$pkgname-$pkgver.tgz")
sha512sums=('c43c65186eacf4b55f30d41ec5ab677b46cc52bc326324e66bd702d386fcdb36c4305a32f2bc5295a83879461817ef9384cc6f269e7bed693eb80bf49a346c36')
# validpgpkeys=()


# prepare() function.  Use for preparing sources ready for compilation
# prepare() {
# 
# }

# pkgver() function.  Use when needing to update pkgver variable during a
# makepkg stage
# pkgver() {
# 
# }

# build() function.  Use to compile the software
# build() {
# 
# }

# check() function. Us to run any checks provided by the software authors
# check() {
# 
# }

# package() function. Use to put the compiled files in a directory where
# makepkg can retrieve them to create a package. 
package() {
    npm install -g --prefix "${pkgdir}/usr" "${srcdir}/${pkgname}-${pkgver}.tgz"

    # npm gives ownership of ALL FILES to build user
    # https://bugs.archlinux.org/task/63396
    chown -R root:root "${pkgdir}"
}