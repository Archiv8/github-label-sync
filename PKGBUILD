#!/bin/bash

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154

# Maintainer: Ross Clark <https://github.com/Archiv8/github-label-sync/discussions>
# Contributor: Ross Clark <https://github.com/Archiv8/github-label-sync/discussions>

# New variables

# Official variables
# pkgbase=""
pkgname="github-label-sync"
pkgdesc="Synchronise GitHub labels with as few destructive operations as possible"
pkgver=2.2.0
pkgrel=1
# epoch=
url="https://github.com/Financial-Times/github-label-sync"
# license=("")
arch=(
  "any"
)
# groups=()
depends=(
  "nodejs"
)
makedepends=(
  "npm"
)
# checkdepends=()
# optdepends=()
# provides=()
# conflicts=()
# replaces=()
# backup=()
options=(
  "!emptydirs"
)
# install=
# changelog="CHANGELOG.md"
source=(
  "https://registry.npmjs.org/$pkgname/-/$pkgname-$pkgver.tgz"
)
noextract=(
  "$pkgname-$pkgver.tgz")

sha512sums=(
  "e0505cc00ffa5e142d15667ffb193020024a9fb5c99642c15c0f9e037923249e984c56d3ca753a0a0f6850ddd15d4081a15d81edf872121a8de88c163bf85fde"
)
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
# [ToDo]: Use jq etc.
package() {

  npm install -g --prefix "${pkgdir}/usr" "${srcdir}/${pkgname}-${pkgver}.tgz"

  # npm gives ownership of ALL FILES to build user
  # https://bugs.archlinux.org/task/63396
  chown -R root:root "${pkgdir}"
}
