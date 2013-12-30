OpenSSL-Vitamio
================

This is a version of the official Android openssl sources, but it is meant to be built as a standalone library to be embedded into app.

To build:
cd openssl-vitamio
/path/to/android-ndk-r9c/ndk-build


Updating the upstream code
-------------------------

This repository tracks the Android openssl repository:
 https://android.googlesource.com/platform/external/openssl/

To use this, add it as a remote called 'upstream'
 git remote add upstream https://android.googlesource.com/platform/external/openssl

Then here's how you get the updated code:
 git checkout upstream (switch to upstream tracking branch)
 git pull upstream master (get newest code from Android, but don't merge)
 git checkout master
 git merge upstream (merge the changes from upstream)
 git push origin master
 git push origin upstream (update the upstream branch)
