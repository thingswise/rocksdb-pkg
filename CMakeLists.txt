cmake_minimum_required(VERSION 3.9)

set(CPACK_PACKAGE_NAME librocksdb-tw)
set(CPACK_PACKAGE_VERSION 5.8.0)
set(CPACK_PACKAGE_CONTACT "info@thingswise.com")

include(CPack)
include(../yap.cmake)

yap_init()
yap_retrieve(git+https://github.com/facebook/rocksdb VERSION 5.8 TAG v5.8)

# staj-c has CMakeLists.txt, but no yap-config.cmake, so provide the hint to the
# package manager
yap_require(git+https://github.com/facebook/rocksdb VERSION 5.8)

