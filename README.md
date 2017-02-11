# Dachshund Tab Layout
[![](https://img.shields.io/badge/minSDK-15-brightgreen.svg)](https://developer.android.com/training/basics/supporting-devices/platforms.html)
[![](https://jitpack.io/v/Andy671/Dachshund-Tab-Layout.svg)](https://jitpack.io/#Andy671/Dachshund-Tab-Layout)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## Introduction
Boosted Android Tab Layout with custom animated indicators including "Dachshund" animation inspired by [this](https://material.uplabs.com/posts/tab-interaction). 

## Sample
![](http://i.giphy.com/1VVYHwT4OFf6U.gif)

## Installation

### Step 1
Add the JitPack repository to your build file
```gradle
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

### Step 2
Add the dependency
```gradle
	dependencies {
		compile 'com.github.Andy671:Dachshund-Tab-Layout:v0.2.0'
	}
```

# Usage
DachshundTabLayout is a subclass of TabLayout, so usage is pretty similar. The most of the original methods should work without any problems. See sample and source code for more info.

Add DachshundTabLayout to xml (after the Toolbar in the AppBarLayout), if you have TabLayout simply replace it: 
```xml
 <android.support.design.widget.AppBarLayout
 ...
	<android.support.v7.widget.Toolbar           
	.../>
	<com.kekstudio.dachshundtablayout.DachshundTabLayout
		android:id="@+id/tab_layout"
		android:layout_width="match_parent"
		android:layout_height="wrap_content"/>
```

Setup it with a ViewPager:
```java
	DachshundTabLayout tabLayout = (DachshundTabLayout) findViewById(R.id.tab_layout);
	tabLayout.setupWithViewPager(yourViewPager);
```

If you want to change animated indicator:
```java
	//AvailableAnimatedIndicator - change it with available animated indicator (see table below)

	AvailableAnimatedIndicator indicator = new AvailableAnimatedIndicator(tabLayout);
	tabLayout.setAnimatedIndicator(indicator);
```

## Available Animated Indicators
| Indicator         	| Custom behavior                         |
|--------------------- 	|--------------------------------|
| DachshundIndicator 	| |
| PointMoveIndicator	| setInterpolator(TimeInterpolator interpolator)|
| LineMoveIndicator 	| |

## XML Attributes
| Attribute        	| Type                | Default     |
| ----------------------|:-------------------:| :-----------|
| ddIndicatorHeight   	| dimension           | 6dp 	    |	
| ddIndicatorColor    	| color               | Color.WHITE |
| ddAnimatedIndicator 	| enum [dachshund, pointMove, lineMove] | dachshund |

## Contribution
- Feel free to fork the repo, make pull requests or fix existing bug
- Feel free to open issues if you find some bug or unexpected behaviour

## Buy me a cup of coffee
> Bitcoin Wallet: 15BuUMAW2jUdStPVkoNPt85P8tJnAy5vD4
