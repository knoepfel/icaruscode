
art_make(
  EXCLUDE
    "ICARUSsplitInductionChannelMapSetupTool_tool.cc"
    "ICARUSsingleInductionChannelMapSetupTool_tool.cc"
  SUBDIRS "details"
  MODULE_LIBRARIES
    larcorealg_Geometry
    ${ART_FRAMEWORK_CORE}
    ${ART_ROOT_IO}
    ${ART_FRAMEWORK_MODULES}
    ${ART_FRAMEWORK_PRINCIPAL}
    ${ART_FRAMEWORK_SERVICES_REGISTRY}
    ${ART_ROOT_IO_TFILE_SUPPORT} ${ROOT_CORE}
    ${ART_ROOT_IO_TFILESERVICE_SERVICE}
    ${BOOST_LIB}
    ${FHICLCPP}
  LIB_LIBRARIES
    larcorealg_Geometry
    larcorealg_CoreUtils
    ${MF_MESSAGELOGGER}
    ${CETLIB}
    ${CETLIB_EXCEPT}
    ${FHICLCPP}
    ${ROOT_GEOM}
    ${ROOT_GENVECTOR}
    ${ROOT_BASIC_LIB_LIST}
  SERVICE_LIBRARIES
    icaruscode_Geometry
    ${ART_UTILITIES}
    ${MF_UTILITIES}
    ${FHICLCPP}
    ${CETLIB}
    ${CETLIB_EXCEPT}
    ${ROOT_GEOM}
    ${ROOT_XMLIO}
    ${ROOT_GDML}
    ${ROOT_BASIC_LIB_LIST}
    
  )


simple_plugin(ICARUSsplitInductionChannelMapSetupTool "tool"
  icaruscode_Geometry
  larcorealg_Geometry
  )
simple_plugin(ICARUSsingleInductionChannelMapSetupTool "tool"
  icaruscode_Geometry
  larcorealg_Geometry
  )


add_subdirectory(gdml)

install_headers(SUBDIRS "details")
install_fhicl(SUBDIRS "details")
install_source(SUBDIRS "details")


