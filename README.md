# Simple Settings

## Download
**Step 1.** Add it in your root *build.gradle* at the end of repositories:
```gradle
allprojects {
	repositories {
		maven { url "https://jitpack.io" }
	}
}
```
**Step 2.** Add the dependency
```gradle
dependencies {
	compile 'com.github.marcellogalhardo:SimpleSettings:0.1.1'
}
```
That's it!

## Using

### Simple Usage

#### Set APP Default Settings
```java
SimpleSettings settings = new SimpleSettings.Builder()
  .baseUrl("www.google.com.br")
  .timeout(20)
  .build();
SimpleSettingsHelper.putDefaultSettings(MainActivity.this, settings);
```

#### Start Simple Settings Activity
```java
if (BuildConfig.DEBUG) {
  SimpleSettingsHelper.startSettingsActivity(MainActivity.this);
}
```

#### Get Settings
```java
SimpleSettings settings = SimpleSettingsHelper.getSimpleSettings(context);
String baseUrl = settings.getBaseUrl();
int timeout = settings.getTimeout();
```

## Credits
If you think you can improve it do not be shy to make your Fork / Pull Request. I will love analyzing improvements to this code.

## Pictures
![Settings-Http](https://github.com/marcellogalhardo/SimpleSettings/blob/master/images/settings-http.png)
![Settings-General](https://github.com/marcellogalhardo/SimpleSettings/blob/master/images/settings-general.png)
![Settings-Screen](https://github.com/marcellogalhardo/SimpleSettings/blob/master/images/settings-screen.png)
![Settings-Options](https://github.com/marcellogalhardo/SimpleSettings/blob/master/images/settings-options.png)
![Settings-Options-Copy](https://github.com/marcellogalhardo/SimpleSettings/blob/master/images/settings-options-copy.png)
![Settings-Options-Share](https://github.com/marcellogalhardo/SimpleSettings/blob/master/images/settings-options-share.png)

## License

Copyright 2016 Marcello Galhardo

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License.
You may obtain a copy of the License at: [here](http://www.apache.org/licenses/LICENSE-2.0).

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
