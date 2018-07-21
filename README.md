# hybrid-base

> A Vue.js project

## Build Setup

``` bash

https://itnext.io/make-hybrid-platform-cordova-vue-webpack-2fb7031c4f9b
https://github.com/F1LT3R/hybrid-base-cordova-vue-webpack

# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test

```

## --- android setup (optional) ---

@powershell -NoProfile -ExecutionPolicy unrestricted -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin

choco install jdk8 -y

choco install android-sdk -y

# will install platform, tools, etc... for android-25
.\sdkmanager "platform-tools" "platforms;android-25" "build-tools;27.0.3" "extras;android;m2repository" "extras;google;m2repository"
.\sdkmanager "emulator" 
.\sdkmanager "system-images;android-25;google_apis;x86"

# start android studio
  # start sdk manager
  - change the path of the sdk C:\Android\android-sdk
    - suppose to have Android 7.1.1 (Nougat) 
      - Android SDK platform 25
      - Google API x86 Atom system image

  # start avd manager
  - device definition, next--
  - select system image nougat api 25, next--
  - graphics: hardware, change mem, camera, netwok, etc... 

  suppose to create file in C:\Users\{username}\.android\avd\{devicename}

# start the emulator, important: not the one from tool
# pick one from the utils 
.\avdmanager.bat list avd 
.\emulator.exe -avd {emulatorname}


## Cordova setup
``` bash

# cmd:
cordova platform add android

# cmd:
# this setup use api 26 so it will probably install it on run since we loaded api 25 in the script above
# todo: should check for a lower version and change all the config files

cordova run android

```


For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
