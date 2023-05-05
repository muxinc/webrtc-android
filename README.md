# webrtc-android

Makes the libwebrtc build from https://github.com/muxinc/webrtc-builder accessible via our Maven repo.

Most consumers should access this like:
```
api 'com.mux:webrtc-android:104.5112.09'
```

## Releasing a new version
* Follow the steps to build a new libwebrtc in https://github.com/muxinc/webrtc-builder 
* Update the VERSION_NAME in gradle.properties in this repo to match the version needed from webrtc-builder
* Tag the update with a pattern such as v104.5112.09 (i.e. start with a 'v') and push to github

For example:
```
git commit -a -m "Update to 104.5112.09"
git push
git tag -a v104.5112.09 -m "v104.5112.09"
git push origin --tags
```

Update your consuming application to use the new version. You can also check on jfrog to see if the package became available.