[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?maxAge=3600)](https://raw.githubusercontent.com/mpusz/conan-google-benchmark/master/LICENSE)
[![Travis CI](https://img.shields.io/travis/mpusz/conan-google-benchmark/master.svg?label=Travis%20CI)](https://travis-ci.org/mpusz/conan-google-benchmark)
[![AppVeyor](https://img.shields.io/appveyor/ci/mpusz/conan-google-benchmark/master.svg?label=AppVeyor)](https://ci.appveyor.com/project/mpusz/conan-google-benchmark)
[![Download](https://api.bintray.com/packages/mpusz/conan-mpusz/google-benchmark%3Ampusz/images/download.svg)](https://bintray.com/mpusz/conan-mpusz/google-benchmark%3Ampusz/_latestVersion)

# conan-google-benchmark

[conan-mpusz](https://bintray.com/mpusz/conan-mpusz) package for [Google Benchmark](https://github.com/google/benchmark) library.

The package generated with this **conanfile** can be found at [conan-mpusz](https://bintray.com/mpusz/conan-mpusz/google-benchmark%3Ampusz).

`conan` client can be downloaded from [Conan.io](https://conan.io).

## Reuse the package

### Add conan-mpusz remote

To add [conan-mpusz](https://bintray.com/mpusz/conan-mpusz) remote to your
local `conan` instance run:

```bash
conan remote add conan-mpusz https://bintray.com/mpusz/conan-mpusz
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
google-benchmark:testing=False
google-benchmark:exceptions=True
google-benchmark:exceptions=False

[generators]
cmake_paths
```

or if you are using `conanfile.py` file add:

```python
requires = "google-benchmark/1.4.1@mpusz/stable"
```

Complete the installation of requirements for your project running:

```
conan install . --build=missing <your_profile_and_settings>
```

Project setup installs the library (and all its dependencies) and generates
`conanbuildinfo.cmake` file with all the necessary paths and variables
needed to link with other dependencies.


## Build package

```
$ conan create . <username>/<channel> <your_profile_and_settings>
```

## Upload package to server

```
$ conan upload -r <remote-name> --all google-benchmark/1.4.1@<username>/<channel>
```
