libssh2 - SSH2 library
======================

libssh2 is a library implementing the SSH2 protocol, available under
the revised BSD license.

Web site: https://www.libssh2.org/

Mailing list: https://cool.haxx.se/mailman/listinfo/libssh2-devel

License: see COPYING

Source code: https://github.com/libssh2/libssh2

Web site source code: https://github.com/libssh2/www

Installation instructions are in:
 - docs/INSTALL_CMAKE for CMake
 - docs/INSTALL_AUTOTOOLS for Autotools

# libssh2-1.8.0-cust
This is a fork of libssh2, version 1.8.0.

Customization is to support download media files from SFTP server, together with vlc-android.

## Please follow below steps to take effect.
1. cp /root/mit/libssh2-1.8.0/src/sftp.h /root/vlc-android/vlc/contrib/contrib-android-arm-linux-androideabi/ssh2/src/sftp.h
2. cp /root/mit/libssh2-1.8.0/src/sftp.c /root/vlc-android/vlc/contrib/contrib-android-arm-linux-androideabi/ssh2/src/sftp.c
3. touch /root/vlc-android/vlc/contrib/contrib-android-arm-linux-androideabi/ssh2
4. cd /root/vlc-android
5. buildsystem/compile.sh -a armeabi-v7a --release -b
6. APK /root/vlc-android/vlc/build-android-arm-linux-androideabi/ndk/libs/armeabi-v7a/libvlc.so
