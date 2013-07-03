v8
==

Google's Javascript Engine

Original instructions for building on Windows with Cygwin

svn co http://src.chromium.org/svn/trunk/deps/third_party/cygwin@66844 third_party/cygwin
python build/gyp_v8

or

python build/gyp_v8 -Dtarget_arch=x64

unset temp
unset tmp

/cygdrive/c/Program\ Files\ \(x86\)/Microsoft\ Visual\ Studio\ 10.0/Common7/IDE/devenv.com /build Release build/all.sln


Comments
--------

The unsets are used because cygwin adds new vars which are lowercase, making the build fail.
If it doesn't work simply kill all the processes called MSBuild.exe you have open and it will work

Building the x64 one requires you to set the current build platform to x64 in Visual Studio.
