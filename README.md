# Android Dependencies Retreiver

Gradle project to analyse Android project and output a dependency file with what need to be installed.

Developed for CI, to allow download Android dependencies without using android-sdk-manager tool.

# Usage

```
git clone git@github.com:jgsqware/android-dependencies-retreiver.git
```

```
cd android-dependencies-retreiver
cp -R <MY-PROJECT-FOLDER> .
```

```
gradle
```

# Example of output

```json
{
    "projects": [
        {
            "dataBinding": true,
            "support": false,
            "name": ":Gradle-Hello-World",
            "compileSdkVersion": "android-22",
            "buildToolsVersion": "23.0.2",
            "targetSdkVersion": 22
        },
        {
            "dataBinding": false,
            "support": true,
            "name": ":Gradle-Hello-World:app",
            "compileSdkVersion": "android-21",
            "buildToolsVersion": "21.0.2",
            "targetSdkVersion": 21
        }
    ]
}
```