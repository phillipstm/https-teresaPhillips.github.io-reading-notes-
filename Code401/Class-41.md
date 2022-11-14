# React Native

## getting started with react native

<https://facebook.github.io/react-native/docs/getting-started>

Name three Core Components of React Native and describe what they do.

    View
    text
    image

What problem does React Native solve (why call it native)?

React Native comes with a set of essential, ready-to-use Native Components you can use to start building your app today. These are React Native's Core Components.

What are the building blocks of a React Native app? How does that compare to a React app?

Components because React Native uses the same API structure as React components, you’ll need to understand React component APIs to get started.

## expo

<https://expo.io/>

What solution does expo provide?

Writing code just once for any mobile interface.

Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the ____ workflow.

Managed

What is the difference between React Native and Expo?

React Native is an library while Expo is a whole framework.

## expo snack

<https://snack.expo.io/>

Checkout this tool. What does snack allow you to do?

It's an open-source platform for running React Native apps in the browser. You can write React Native code and run it directly in Expo Go or even in the browser.

## ejecting

<https://docs.expo.io/versions/latest/expokit/eject>

What does “eject” mean within the context of Expo?

Expo allows you to eject your pure-JS project from the Expo iOS/Android clients, providing you with native projects that can be opened and built with Xcode and Android Studio. Those projects will have dependencies on ExpoKit, so everything you already built will keep working as it did before.

When should you not eject?

-All you need is to distribute your app in the iTunes Store or Google Play. Expo can build binaries for you in that case. If you eject, we can't automatically build for you any more.

-You are uncomfortable writing native code. Ejected apps will require you to manage Xcode and Android Studio projects.

-You enjoy the painless React Native upgrades that come with Expo. After your app is ejected, breaking changes in React Native will affect your project differently, and you may need to figure them out for your particular situation.

-You require Expo's push notification services. After ejecting, since Expo no longer manages your push credentials, you'll need to manage your own push notification pipeline.

-You rely on asking for help in the Expo community. In your native Xcode and Android Studio projects, you may encounter questions which are no longer within the realm of Expo.

Why might you choose to eject?

Your Expo project needs a native module that Expo doesn't currently support. We're always expanding the Expo SDK, so we hope this is never the case. But it happens, especially if your app has very specific and uncommon native demands.
