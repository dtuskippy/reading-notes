# Class-41 -- React Native

This is the topic of the week, and a pretty hot topic in React land.

## [getting started with react native](https://reactnative.dev/docs/getting-started)

1. Name three Core Components of React Native and describe what they do.
    * View: A container that supports layout with flexbox, style, some touch handling, and accessibility controls.
    * Text: Displays, styles, and nests strings of text and even handles touch events.
    * Image: Displays different types of images.
    * ScrollView: A generic scrolling container that can contain multiple components and views.
    * TextInput: Allows the user to enter text.
2. What problem does React Native solve (why call it native)?
    * It attempts to be the 'write once, run everywhere'-solution.
    * React Native is an open-source platform created in JavaScript by Facebook
    * It enables you to build mobile apps for both Android and iOS operating systems -- they can work on any device and still use one codebase only.
    * Native app is made to work on a particular operating system. That means they can use all the blessings of that system, yet it cannot work anywhere else besides.
        * So React Native claims to be a multi-platform environment with the functionality of native.
3. What are the building blocks of a React Native app? How does that compare to a React app?
    * React Native is basically React with Native specific components.

## [expo](https://expo.dev/)

1. What solution does expo provide?
    * Expo is a set of tools and services (framework / platform) built around React Native and, while it has many features, the most relevant feature for us right now is that it can get you writing a React Native app within minutes. 
    * You will only need a recent version of Node.js and a phone or emulator.
2. Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the ____ workflow.
    * “Managed workflow” is when you let Expo handle specifying important properties through a convenient app.json, as well build your app on their servers.
    * A “bare workflow” is when you’re not solely restricted to the “Expo ecosystem,” and thus are free to do more customization to your app. [Source](https://medium.com/@natesabrown/deciding-between-expo-managed-bare-workflows-1e69af847003)
3. What is the difference between React Native and Expo?
    * React Native is the library developed by Meta and Expo is a framework/platform to develop React Native apps.

## [expo snack](https://snack.expo.dev/)

1. Checkout this tool. What does snack allow you to do?
    * Basically a form of sandbox that allows you to instantly view changes you make to a basic code base.

## [ejecting](https://docs.expo.dev/expokit/eject/?redirected)

1. What does “eject” mean within the context of Expo?
    * In cases where advanced developers need native capabilities not supported by React Native Core or the Expo SDK, Expo allows you to eject your pure-JS project from the Expo iOS/Android clients, providing you with native projects that can be opened and built with Xcode and Android Studio.
2. When should you not eject?
    * All you need is to distribute your app in the iTunes Store or Google Play. Expo can build binaries for you in that case. If you eject, we can't automatically build for you any more.
    * You are uncomfortable writing native code. Ejected apps will require you to manage Xcode and Android Studio projects.
    * You enjoy the painless React Native upgrades that come with Expo. After your app is ejected, breaking changes in React Native will affect your project differently, and you may need to figure them out for your particular situation.
    * You require Expo's push notification services. After ejecting, since Expo no longer manages your push credentials, you'll need to manage your own push notification pipeline.
    * You rely on asking for help in the Expo community. In your native Xcode and Android Studio projects, you may encounter questions which are no longer within the realm of Expo.
3. Why might you choose to eject?
    * Your Expo project needs a native module that Expo doesn't currently support.

## Tutorial

1. [react native basics](https://reactnative.dev/docs/tutorial)

## Bookmarks

1. [react native](https://reactnative.dev/)

## Additional Questions

1. Looking ahead at this module’s course schedule, What do you look forward to learning?
    * Both mobile development and open source.
2. What are your learning goals after reading and reviewing the class README?
    * Get the basics of React Native.

## Things I want to know more about

1. React Native is a complex topic I have barely scratched the surface of, so plenty more to dig into.
