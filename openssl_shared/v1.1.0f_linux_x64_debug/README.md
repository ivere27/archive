```
// openssl version
openssl OpenSSL_1_1_0f

// gcc --version
gcc (Ubuntu 5.4.0-6ubuntu1~16.04.4) 5.4.0 20160609
...

// openssl build command
$ ./Configure -g linux-x86_64 shared no-ssl2 no-ssl3 no-comp no-hw no-engine no-asm no-unit-test

// change openssl's rpath
$ patchelf --set-rpath '.' openssl

$ ldd openssl
	linux-vdso.so.1 =>  (0x00007ffcfe1e1000)
	libssl.so.1.1 => ./libssl.so.1.1 (0x00007f5890b52000)
	libcrypto.so.1.1 => ./libcrypto.so.1.1 (0x00007f5890739000)
	libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007f58904e5000)
	libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f589011b000)
	libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007f588ff17000)
	/lib64/ld-linux-x86-64.so.2 (0x0000561c11805000)
```