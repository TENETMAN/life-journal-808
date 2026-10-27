HEIC component source and rebuild information

heic-to 1.6.6 is LGPL-3.0 (not MIT). It contains libheif 1.23.6 and uses libde265 1.0.16 according to the upstream build instructions. The unmodified official source archives are supplied alongside this file, with SHA-256 and original URLs in manifest.json. License texts are in /licenses/HEIC-LGPL-3.0.txt and /licenses/GPL-3.0.txt and inside the archives.

Source: https://github.com/hoppergee/heic-to/tree/4045b8d7607e326c2b479cc424c7a60519b42dae
libheif: https://github.com/strukturag/libheif/tree/v1.23.6
libde265: https://github.com/strukturag/libde265/tree/v1.0.16

The application does not prohibit reverse engineering for debugging changes to LGPL libraries. You may replace the HEIC component and rebuild the application. Application source, pinned dependencies, configuration examples and build scripts are delivered to the owner in the source package.

Rebuild this app: npm ci; npm run build. To replace the library, extract heic-to source, change it, run the upstream build, install your modified package as the local heic-to dependency, and rebuild. src/lib/images.ts imports heic-to/csp with the heicTo({blob,type,quality}) interface. The library is a separate dynamic chunk. No signature, paid license check or activation prevents replacement. Rebuild the PWA cache manifest and serve your resulting dist directory under your own origin.

Upstream libheif instructions are in its build-emscripten.sh and heic-to README. For the CSP build, upstream documents LIBDE265_VERSION=1.0.16 USE_UNSAFE_EVAL=0 USE_WASM=0. Building that dependency requires its documented compiler/build tools; normal app builds use the pinned published library and do not require a C++ toolchain.
