[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?maxAge=3600)](https://raw.githubusercontent.com/mpusz/conan-google-benchmark/master/LICENSE)
[![Travis CI](https://img.shields.io/travis/mpusz/conan-google-benchmark/master.svg?label=Travis%20CI)](https://travis-ci.org/mpusz/conan-google-benchmark)
[![AppVeyor](https://img.shields.io/appveyor/ci/mpusz/conan-google-benchmark/master.svg?label=AppVeyor)](https://ci.appveyor.com/project/mpusz/conan-google-benchmark)
[![Download](https://api.bintray.com/packages/mpusz/conan-mpusz/google-benchmark%3Ampusz/images/download.svg)](https://bintray.com/mpusz/conan-mpusz/google-benchmark%3Ampusz/_latestVersion)

# DEPRECATED

Please note that as Google Benchmark now has an official Conan support this repository should be considered
deprecated. Please download the latest google benchmark from: https://bintray.com/conan/conan-center/benchmark%3A_.

---

# conan-google-benchmark

[conan-mpusz](https://bintray.com/mpusz/conan-mpusz) package for [Google Benchmark](https://github.com/google/benchmark) library.

The package generated with this **conanfile** can be found at [conan-mpusz](https://bintray.com/mpusz/conan-mpusz/google-benchmark%3Ampusz).

`conan` client can be downloaded from [Conan.io](https://conan.io).

## Reuse the package

### Add conan-mpusz remote

To add [conan-mpusz](https://bintray.com/mpusz/conan-mpusz) remote to your
local `conan` instance run:

```bash
conan remote add conan-mpusz https://api.bintray.com/conan/mpusz/conan-mpusz
```

### Basic setup

```
$ conan install google-benchmark/1.4.1@mpusz/stable --build=missing
```

### Project setup

If you handle multiple dependencies in your project, it would be better
to add a `conanfile.txt`

```
[requires]
google-benchmark/1.4.1@mpusz/stable

[options]

[generators]
cmake_paths
```

or if you are using `conanfile.py` file add:

```python
requires = "google-benchmark/1.4.1@mpusz/stable"
```

Complete the installation of requirements for your project running:

```
mkdir build
cd build
conan install .. --build=outdated <your_profile_and_settings>
<your typical build process>
```

Project setup installs the library (and all its dependencies), and assuming you chose
`cmake_paths` as a generator, it generates `conan_paths.cmake` file that defines variables
to make CMake `find_package()` work and find all the dependencies in the Conan local cache.


## Build package

```
$ conan create . <user>/<channel> <your_profile_and_settings>
```

## Upload package to server

```
$ conan upload -r <remote-name> --all google-benchmark/1.4.1@<user>/<channel>
```
