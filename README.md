# wxjson-modern-build

This is a copy of https://luccat.users.sourceforge.net/wxjson/ with minor fixes to make it work with wxWidgets 3.1.5+. 

I'm not the author of wxJSON, all the credit goes to L. Cattani.

The CMake script requires the CMake's Findwxwidgets script to be able to locate wxWidgets library: you need to either have it in your system or use ExternalProject_Add. See https://github.com/lszl84/wx_cmake_template.git 