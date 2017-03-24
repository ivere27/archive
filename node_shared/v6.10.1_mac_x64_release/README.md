```
$ ./configure --shared

$ system_profiler SPSoftwareDataType
Software:
    System Software Overview:
      System Version: macOS 10.12.3 (16D32)
      Kernel Version: Darwin 16.4.0
...

$ c++ --version
Apple LLVM version 8.0.0 (clang-800.0.42.1)
Target: x86_64-apple-darwin16.4.0
Thread model: posix
InstalledDir: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin


$ strip -S <all files>
```
