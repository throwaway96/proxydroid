# ProxyDroid

This is my personal copy of ProxyDroid. It's not currently intended for anyone else to use, but if you want to try, go ahead. It's basically untested.

## Issues

* Since Android 10, non-system apps are not allowed to get a list of configured Wi-Fi networks using [`WifiManager.getConfiguredNetworks()`](https://developer.android.com/reference/android/net/wifi/WifiManager#getConfiguredNetworks()). I might be able to target an older API level, although I'm not sure that will even work on Android 11. Regardless, there would need to be some code to prompt for the fine location permission and handle rejection. I didn't feel like writing that, so I just commented the call out.
* I added some missing translations that lint was complaining about. Since I don't speak the relevant languages, I have no idea whether any of it is correct.

## Building

* Gradle 8.7 doesn't work with JDK 22, so I've been using JDK 21. You may have to set `JAVA_HOME`.
* Set `ANDROID_HOME` to your Android SDK directory (should contain `platforms`, `ndk` dirs).
* Run `./gradlew build`.
* Maybe some other stuff I'm forgetting.

```sh
export ANDROID_HOME=/usr/lib/android-sdk
./gradlew build
```

## Dependencies

Includes the following software:

* libevent - an event notification library (3-clause BSD): <https://libevent.org/>
* redsocks - transparent socks redirector (Apache 2.0): <https://darkk.net.ru/redsocks/>
* termExec - JNI layer for executing stuff (Apache 2.0): AOSP

## License

This program is free software: you can redistribute it and/or modify it under the terms of version 3 of the GNU General Public License as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program (see `COPYING`). If not, see <https://www.gnu.org/licenses/>.
