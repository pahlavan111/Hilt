# Hilt
First, add the hilt-android-gradle-plugin plugin to your project's root build.gradle file:
    buildscript {
        ...
        dependencies {
            ...
            classpath 'com.google.dagger:hilt-android-gradle-plugin:2.28-alpha'
        }
    }


Then, apply the Gradle plugin and add these dependencies in your app/build.gradle file:
    ...
    apply plugin: 'kotlin-android'
    apply plugin: 'kotlin-android-extensions'    //check this 2 upper plugin that what it is
    apply plugin: 'kotlin-kapt'
    apply plugin: 'dagger.hilt.android.plugin'

    android {
        ...
    }

    dependencies {
        implementation "com.google.dagger:hilt-android:2.28-alpha"
        kapt "com.google.dagger:hilt-android-compiler:2.28-alpha"
    }

Hilt uses Java 8 features. To enable Java 8 in your project, add the following to the app/build.gradle file:

    android {
      ...
      compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
      }

          kotlinOptions {
            jvmTarget = JavaVersion.VERSION_1_8.toString()
        }
      }
