# for classes_def.xml!!
include_directories( ${CMAKE_CURRENT_SOURCE_DIR} )
include_directories( $ENV{NURANDOM_INC} )

art_make( 
          LIBRARY_NAME icaruscode_CRTProducts
          LIB_LIBRARIES
                        ROOT::Core
                        ROOT::EG
        )

install_headers()
install_fhicl()
install_source()
