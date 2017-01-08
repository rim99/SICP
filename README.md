# SICP

SCIP is a famous textbook of computer science contributed from the MIT.

This repo contains the original and Chinese-translated version textbooks, and the source code of excerise environment for Unix.

## Building MIT/GNU Scheme from portable C on unix

This page describes how to generate binaries from the portable C sources. These binaries should run with little or no trouble on most modern architectures and operating systems. It will probably require tweaking for systems that haven't been tested.

When built this way, the system runs slower than when it is built using the native-code compiler. For this reason, you will usually want to use native-code binaries when running on a supported architecture. However, on 32-bit architectures, the portable-code binaries can address larger amounts of virtual memory than the native-code binaries, so it is reasonable (and supported) to use both kinds on the same machine.

1. Download the portable C source package mit-scheme-c-9.2.tar.gz.
2. Unpack the source package:

	```
	tar xzf mit-scheme-c-9.2.tar.gz
	cd mit-scheme-c-9.2/src
	```
	
3. Build the package:

	```
	etc/make-liarc.sh
	```

	This will take a long time; on fairly fast machines with lots of RAM it takes about an hour. On older machines it will take longer or fail altogether, at which point you should ask for help. Note that you can pass configure options to the script, such as
	
	```
	etc/make-liarc.sh --help
	```
	or
	
	```
	etc/make-liarc.sh --prefix=/usr
	```
4. Install the program:
	
	```
	make install
	```
	Depending on configuration options and file-system permissions, you may need super-user privileges to do the installation step. 