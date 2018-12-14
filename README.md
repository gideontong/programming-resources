# Programming Resources

This document is a compilation of the programming resources recommended by Gideon Tong for creating a user-facing software project. It contains information on software for creating certain types of software projects as well as tutorials for first-time programmers.

## Mobile App

Mobile apps are apps that run on mobile platforms, typically ARM-based processors with touchscreens like iOS-based iPhones and iPads or Android-based smartphones and tablets.

### Cross-Platform

Cross-platform apps are apps that use one code base but can run on multiple types of devices at the same time, like iOS and Android.

#### C#

C# is a multipurpose programming language based on C that supports objects and functions. You can build apps in C# using [Xamarin](http://bit.ly/2LhvNd4). It uses native UI elements and hardware, so you can easily interface with hardware-based APIs or even platform-specific APIs. You can use Xamarin on Windows, macOS, or Linux, but to build apps for iOS you'll need to install Xamarin on a macOS computer.

#### JavaScript

JavaScript is a high-level programming language that is considered dynamic and runs in a web browser like Google Chrome. You can build cross-platform mobile apps using a framework like [React Native](http://bit.ly/2UMM4uL). It still supports native code for platform-specific functions, but runs dynamically and is super easy to quickly build.

To get started, you'll need a computer running Windows, macOS, or Linux with [Node.js](http://bit.ly/2PFnEQ6) installed (simply download either the LTS or current version, with the current version being more bleeding edge). You can run apps instantaneously with instant debugging if you install the [Expo](http://bit.ly/2RY0xCk) app on your phone ([iOS](https://apple.co/2EjZMQ1) & [Android](http://bit.ly/2BkMEXN)). To build apps for iOS, you'll need to install React Native on a macOS computer.

### iOS

iOS apps require you to build using a macOS computer. However, there are ways to test your app without a macOS computer if you are using JavaScript, for example. To publish your app on the Apple App Store, you'll need to pay $99 per year as well as own a macOS computer with a development certificate (note that this is not per person, but there are additional steps required if you are going to share the same developer account within a group).

#### Objective-C

Objective-C is another multipurpose object-oriented programming language based on C. It is older than Swift and tends to be used for older iOS libraries and iOS app projects. It is supported by [Xcode](https://apple.co/2QXBNNc), although many of the newer code projects now default to using Swift.

If you'd like to get started with Objective-C anyways, the Apple documentation begins with [this link](https://apple.co/2QUhgct).

#### Swift

[Swift](https://apple.co/2QZjQ17) is another multipurpose object-oriented programming language designed to be easy to learn and powerful enough to prevent against mistakes from inexperienced programmers.

### Android

Android apps can be built using a multitude of tools, and can even be created using an iOS or Android device. They are super powerful and offer more flexibility and hardware APIs than iOS apps do. To publish an app on the Google Play Store, you'll need to pay a one-time fee of $25 as well as have access to a web browser to upload your app.

#### Java

#### Kotlin

## Website

Websites are easy to update and allow dynamic updating, and are also easy to build and do not take long to create a basic version (like an MVP!) of a website. They need to be hosted on a server somewhere, and a website builder like Google Sites or GitHub Pages does the hosting automatically for you. However, if you are not serving static content, it is not recommended to use a web host that does not allow you access to the server.

### Dynamic Content

Dynamic content is data that changes based on who sees it or what is entered into it. This might include things like a login system, forums, user profiles, or other platforms that changes who is looking at it or what people want to see.

### Static Content

Static content is information that is defined and doesn't change on a day-to-day basis. It might be good for webstores, informational websites, blogs, and other platforms (however, a blog would be better hosted on an existing hosting service).

There isn't a lot of programming in creating a static content, instead, you should instead just download a template and create a website with a drag-and-drop WYSIWYG (what you see is what you get) editor.

## Desktop App

### Cross-Platform

### Windows

### macOS

### Linux/UNIX

## Browser Extension

Browser extensions are small JavaScript-based applets that within your web browser in order to run scripts or modify the website data.

### Cross-Platform

### Google Chrome

### Mozilla Firefox

### Apple Safari

### Microsoft Edge

You shouldn't build an extension exclusively for Microsoft Edge. It is being phased out of development by Microsoft and will not be supported by them in the near future.