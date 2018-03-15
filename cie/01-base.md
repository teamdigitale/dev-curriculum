

# Hacking on CIE-NIS-CPP-SDK

CIE-NIS-CPP-SDK is a collection of libraries written in C++ to leverage the Italian Electronic Identity Card (CIE) facilities. This SDK specifically targets reading the Service Identifier Number (NIS) from a CIE. 

With this activity you will learn how to hack and contribute on this toolkit.

# Prerequisites

In order to hack on the sdk, you have to first download the source code and install any missing dependencies. The focus of this lab is to develop on Linux OS, so you need any recent Linux distro or VM (in this lab we used Ubuntu):

* Install the development package of pcsc-lite for your distro: `sudo apt-get install libpcsclite-dev`
* Clone the repo: `git clone https://github.com/italia/cie-nis-cpp-sdk.git`
* Rebuild the CIE SDK: `make && make doc`
* Connect the smartcard reader and launch the PCSC daemon: `sudo pcscd`

If you performed all the instructions correctly, you wil be able to see the daemon running: `ps aux|grep pcscd`.
Should the daemon not appear in the list, please verify that the reader is connected (usually through USB), that the device can be seen by Linux (if you're on a VM, you should probably connect the USB device through your VM host settings: `lsusb`) and that you have entered the correct credentials as sudo (the daemon has to run as root, the examples need not).

# Identifying a task and Hacking

The very first task should be to run the example program (launch `bin/test-nis`, source code is in `src/test/example-nis.cpp`) that read the NIS back from the CIE. To do this you should first compile the SDK, then run the test program. Remember that the card must be placed on behalf the reader, since it's an NFC device. If all goes well the test program should print out the NIS number.

Once the test program works, if you feel brave and want to contribute more you can find a list of all features where you can contribute [on the relevant issues page](https://github.com/italia/cie-nis-cpp-sdk/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aopen++). You can take on any task with the `help wanted` label.

If you feel extraordinarily-brave, you can take on the refactor of an old test program (`src/test/example-verify.cpp`). This program was written before the SDK API got revamped, so the task here is to port the example code to the new API. Some hint  are in order (you deserve it!):

* changes involve both `src/test/example-verify.cpp` and `src/request.cpp`.
* you may want to tweak `src/test/Makefile` to include `example-verify` as a target (it currently won't compile out of a vacuum).
* the very first part of the example code is almost identical to the working example in `src/test/example-nis.cpp`, that you already run in the first step as `bin/test-nis`.

Once you found a task you want to tackle, you can start to work on it.

# Documentation

For more information, make sure to check out our [brief guide and a tour of the API](https://italia.github.io/cie-nis-cpp-sdk/html/), or take a look at the generated doc under `doc/` directory.

# Submitting your work

We'd love to integrate your work in our repositories! Please make sure your local git is configured, so that we can give you proper attribution.

```.bash
git config --global user.name "Your Name"
git config --global user.email your.email@address.org
```

Then [fork](https://github.com/italia/cie-nis-cpp-sdk#fork-destination-box) `cie-nis-cpp-sdk` and submit a Pull Request. If you don't know how to do this, check out [the awesome guide from GitHub](https://help.github.com/articles/creating-a-pull-request/).

Happy hacking!
