# `AndroidTagGroup`

[![Release](https://jitpack.io/v/Eddydpyl/AndroidTagGroup.svg)](https://jitpack.io/#Eddydpyl/AndroidTagGroup)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-AndroidTagGroup-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/1539)

The TagGroup is a special layout with a set of tags. You can use it to tag people, books or anything you want.


# Demo

### Screenshot
![screenshot1](http://ww4.sinaimg.cn/large/bce2dea9jw1esbsby9v5fj20u00w8jxx.jpg)

### Edit Tags
![screenshot2](http://ww4.sinaimg.cn/large/bce2dea9jw1esbsbngv8fj20u005w75v.jpg)
![screenshot3](http://ww4.sinaimg.cn/large/bce2dea9jw1esbsbmoagij20u005sabl.jpg)

[Download Demo](https://github.com/2dxgujun/AndroidTagGroup/releases/download/v1.4/AndroidTagGroup-Demo-v1.4.apk)

# Usage

## Step 1

#### Gradle

  -  Add the following to your project level `build.gradle`:

```gradle
allprojects {
	repositories {
		maven { url "https://jitpack.io" }
	}
}
```
  -  Add this to your app `build.gradle`:

```gradle
dependencies {
	compile 'com.github.Eddydpyl:AndroidTagGroup:1.7.1'
}
```

#### Maven

- Add the following to your `pom.xml`:
```xml
<repository>
       	<id>jitpack.io</id>
	    <url>https://jitpack.io</url>
</repository>

<dependency>
	    <groupId>com.github.Eddydpyl</groupId>
	    <artifactId>AndroidTagGroup</artifactId>
	    <version>1.7.1</version>
</dependency>
```

## Step 2

Use it in your own code:
```xml
<me.gujun.android.taggroup.TagGroup
    android:id="@+id/tag_group"
    style="@style/TagGroup" />
```

```java
TagGroup mTagGroup = (TagGroup) findViewById(R.id.tag_group);
mTagGroup.setTags(new String[]{"Tag1", "Tag2", "Tag3"});
```
Use `setTags(...)` to set the initial tags in the group.

#### How to submit a new tag?

To "submit" a new tag as user press "Enter" or tap the blank area of the tag group, also you can "submit" a new tag via `submitTag()`.

~~**Note**: Google keyboard (a few soft keyboard not honour the key event) currently not supported "Enter" key to "submit" a new tag.~~ **This issue has been fixed in v1.6.0**

#### How to delete a tag?

To delete a tag as user press "Backspace" key or double-tap the tag which you want to delete.

#### How to detect tag click event?

Implement a callback interface: `TagGroup.OnTagClickListener`, and set the listener via `setOnTagClickListener()`.

#### How to use autocomplete?

Use `setAutoCompleteTags()` on the target TagGroup and pass as input parameter the tags you want to use for this purpose.

#### Important changes in v1.7.1

- The new setAllowRepeats() method takes a boolean as input parameter and sets wether or not the user is allowed to submit a new tag when its text is the exact same as the one in any other of the tags in the TagGroup.

# Build

run `./gradlew assembleDebug` (Mac/Linux)

or

run `gradlew.bat assembleDebug` (Windows)

# Attributes

There are several attributes you can set:

![Dimension illustrate](http://ww2.sinaimg.cn/large/bce2dea9gw1epov0i8x6kj20rk054q4g.jpg)

|           attr        	|     default      |                         mean                          	 |
|:------------------------- |:---------------- |:------------------------------------------------------- |
| atg_isAppendMode      	| false            | Determine the TagGroup mode, APPEND or single DISPLAY.  |
| atg_inputHint   	        | Add Tag/????  | The hint of the INPUT tag.                              |
| atg_borderColor	        | #49C120          | The tag outline border color.                           |
| atg_textColor          	| #49C120          | The tag text color.                           	         |
| atg_backgroundColor       | #FFFFFF          | The tag background color.                               |
| atg_dashBorderColor       | #AAAAAA          | The tag dash outline border color.                      |
| atg_inputHintColor        | #80000000        | The input tag hint text color.                          |
| atg_inputTextColor        | #DE000000        | The input tag type text color..                         |
| atg_checkedBorderColor    | #49C120          | The checked tag outline border color.                   |
| atg_checkedTextColor      | #FFFFFF          | The checked text color.                                 |
| atg_checkedMarkerColor    | #FFFFFF          | The checked marker color.                               |
| atg_checkedBackgroundColor| #49C120          | The checked tag background color.                       |
| atg_pressedBackgroundColor| #EDEDED          | The tag background color when the tag is being pressed. |
| atg_borderStrokeWidth     | 0.5dp            | The tag outline border stroke width.        	         |
| atg_textSize          	| 13sp             | The tag text size.                                  	 |
| atg_horizontalSpacing     | 8dp              | The horizontal tag spacing.(Mark1)                      |
| atg_verticalSpacing  	    | 4dp              | The vertical tag spacing.(Mark2)                      	 |
| atg_horizontalPadding	    | 12dp             | The horizontal tag padding.(Mark3)                      |
| atg_verticalPadding  	    | 3dp              | The vertical tag padding.(Mark4)                        |

# Developed By

Jun Gu - <2dxgujun@gmail.com>

<a href="http://weibo.com/2dxgujun">
  <img alt="Follow me on Weibo" src="http://ww4.sinaimg.cn/large/bce2dea9gw1epjhk9h9m6j20230233yb.jpg"/>
</a>
<a href="https://plus.google.com/u/0/113657331852211913645">
  <img alt="Follow me on Google Plus" src="http://ww1.sinaimg.cn/large/bce2dea9gw1epjhbx0ouij2023023jr6.jpg"/>
</a>

# License

    Copyright 2015 Jun Gu

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
