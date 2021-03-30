cmake_minimum_required(VERSION 3.13.4)

project(FlyThrough)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/FlyThrough")
set(EXTENSION_CATEGORY "Virtual Visualization")
set(EXTENSION_CONTRIBUTORS "Andinet Enquobahrie (Kitware)")
set(EXTENSION_DESCRIPTION "This is an extension module with loadable and scripted modules for fly through visualization")
set(EXTENSION_ICONURL "http://www.example.com/Slicer/Extensions/FlyThrough.png")
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/FlyThrough/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(CameraPath)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
