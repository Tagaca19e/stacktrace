Linux Distro
```
NAME="Amazon Linux"
VERSION="2"
ID="amzn"
ID_LIKE="centos rhel fedora"
VERSION_ID="2"
PRETTY_NAME="Amazon Linux 2"
ANSI_COLOR="0;33"
CPE_NAME="cpe:2.3:o:amazon:amazon_linux:2"
HOME_URL="https://amazonlinux.com/"
```

Current problem when running `make -j8 debug`, still trying to figure it out

```
[CORP\etagaca@a-2q1tizyn69lfl 3480-lab1]$ make -j8 debug
g++ -std=c++17 -Wfatal-errors -Werror -D GLEW_STATIC -D FMT_HEADER_ONLY -g -D DEBUG ./obj/debug/Input.o ./obj/debug/InputOutput.o ./obj/debug/StringUtil.o ./obj/debug/Properties.o ./obj/debug/Camera.o ./obj/debug/Texture.o ./obj/debug/Framebuffer.o ./obj/debug/Tool.o ./obj/debug/SoftwareRenderer.o ./obj/debug/main.o ./obj/debug/GraphicsUtils.o ./obj/debug/Application.o ./obj/debug/Prompts.o ./obj/debug/imgui/imgui_draw.o ./obj/debug/imgui/imgui_widgets.o ./obj/debug/imgui/ImSequencer.o ./obj/debug/imgui/ImGuizmo.o ./obj/debug/imgui/imgui_impl_opengl3.o ./obj/debug/imgui/ImGradient.o ./obj/debug/imgui/GraphEditor.o ./obj/debug/imgui/imgui_tables.o ./obj/debug/imgui/imgui.o ./obj/debug/imgui/implot.o ./obj/debug/imgui/ImCurveEdit.o ./obj/debug/imgui/implot_items.o ./obj/debug/imgui/imgui_demo.o ./obj/debug/imgui/implot_demo.o ./obj/debug/imgui/imgui_impl_glfw.o -o ./bin/debug/3480-main -L./lib -lglfw3 -lGL -lGLEW -ldl -lX11 -lpthread 
./obj/debug/InputOutput.o: In function `IO::getFilenamesInFolder(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&, std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&, bool, bool)':
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::~recursive_directory_iterator()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::~recursive_directory_iterator()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::operator*() const'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::operator++()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::~recursive_directory_iterator()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::~recursive_directory_iterator()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::~recursive_directory_iterator()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:129: undefined reference to `std::experimental::filesystem::v1::__cxx11::directory_iterator::operator*() const'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:129: undefined reference to `std::experimental::filesystem::v1::__cxx11::directory_iterator::operator++()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:145: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::has_filename() const'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::~recursive_directory_iterator()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::~recursive_directory_iterator()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:119: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::~recursive_directory_iterator()'
./obj/debug/InputOutput.o: In function `IO::pathOfFile(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&)':
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:264: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::parent_path() const'
./obj/debug/InputOutput.o: In function `IO::createPath(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&)':
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:274: undefined reference to `std::experimental::filesystem::v1::create_directory(std::experimental::filesystem::v1::__cxx11::path const&)'
./obj/debug/InputOutput.o: In function `IO::getAssetRoot[abi:cxx11](int)':
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:282: undefined reference to `std::experimental::filesystem::v1::current_path[abi:cxx11]()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:282: undefined reference to `std::experimental::filesystem::v1::absolute(std::experimental::filesystem::v1::__cxx11::path const&, std::experimental::filesystem::v1::__cxx11::path const&)'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:287: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::parent_path() const'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:293: undefined reference to `std::experimental::filesystem::v1::current_path[abi:cxx11]()'
/home/etagaca/Desktop/3480-lab1/src/InputOutput.cpp:293: undefined reference to `std::experimental::filesystem::v1::canonical(std::experimental::filesystem::v1::__cxx11::path const&, std::experimental::filesystem::v1::__cxx11::path const&)'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::path(std::experimental::filesystem::v1::__cxx11::path&&)':
/usr/include/c++/7/experimental/bits/fs_path.h:185: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::path(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >&&)':
/usr/include/c++/7/experimental/bits/fs_path.h:191: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::clear()':
/usr/include/c++/7/experimental/bits/fs_path.h:297: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::_M_append(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&)':
/usr/include/c++/7/experimental/bits/fs_path.h:399: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::extension() const':
/usr/include/c++/7/experimental/bits/fs_path.h:981: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_find_extension() const'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::has_extension() const':
/usr/include/c++/7/experimental/bits/fs_path.h:997: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_find_extension() const'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::directory_entry::status() const':
/usr/include/c++/7/experimental/bits/fs_dir.h:113: undefined reference to `std::experimental::filesystem::v1::status(std::experimental::filesystem::v1::__cxx11::path const&)'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::directory_iterator::directory_iterator(std::experimental::filesystem::v1::__cxx11::path const&)':
/usr/include/c++/7/experimental/bits/fs_dir.h:188: undefined reference to `std::experimental::filesystem::v1::__cxx11::directory_iterator::directory_iterator(std::experimental::filesystem::v1::__cxx11::path const&, std::experimental::filesystem::v1::directory_options, std::error_code*)'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::recursive_directory_iterator(std::experimental::filesystem::v1::__cxx11::path const&)':
/usr/include/c++/7/experimental/bits/fs_dir.h:269: undefined reference to `std::experimental::filesystem::v1::__cxx11::recursive_directory_iterator::recursive_directory_iterator(std::experimental::filesystem::v1::__cxx11::path const&, std::experimental::filesystem::v1::directory_options, std::error_code*)'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::exists(std::experimental::filesystem::v1::__cxx11::path const&)':
/usr/include/c++/7/experimental/bits/fs_ops.h:127: undefined reference to `std::experimental::filesystem::v1::status(std::experimental::filesystem::v1::__cxx11::path const&)'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::path<std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> >, std::experimental::filesystem::v1::__cxx11::path>(std::__cxx11::basic_string<char, std::char_traits<char>, std::allocator<char> > const&)':
/usr/include/c++/7/experimental/bits/fs_path.h:198: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::path<char const*, std::experimental::filesystem::v1::__cxx11::path>(char const* const&)':
/usr/include/c++/7/experimental/bits/fs_path.h:198: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::path<char [2], std::experimental::filesystem::v1::__cxx11::path>(char const (&) [2])':
/usr/include/c++/7/experimental/bits/fs_path.h:198: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::path<char [8], std::experimental::filesystem::v1::__cxx11::path>(char const (&) [8])':
/usr/include/c++/7/experimental/bits/fs_path.h:198: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
./obj/debug/InputOutput.o: In function `std::experimental::filesystem::v1::__cxx11::path::path<char [7], std::experimental::filesystem::v1::__cxx11::path>(char const (&) [7])':
/usr/include/c++/7/experimental/bits/fs_path.h:198: undefined reference to `std::experimental::filesystem::v1::__cxx11::path::_M_split_cmpts()'
collect2: error: ld returned 1 exit status
make: *** [bin/debug/3480-main] Error 1
[CORP\etagaca@a-2q1tizyn69lfl 3480-lab1]$ 

```