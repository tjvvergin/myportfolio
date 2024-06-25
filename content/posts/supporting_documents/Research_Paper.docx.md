---
title: "Research Paper"
date: 2024-06-25T16:20:31-4:00
draft: false
---

Tyler Vergin

June 1st, 2023

CSC-391

GoDex Pro Research Paper

Abstract:

This paper explores the complex weave of technologies used in the
creation of the GoDex Pro app, a resource for Pokémon Go players. The
use of the data-driven SwiftUI framework, along with Swift Charts and
WebKit functionality, allowed for the development of a dynamic and
engaging user interface. The history of iOS development is also
discussed, tracing its evolution from the use of the Cocoa UI framework
and Objective-C programming language to the introduction of Swift and
SwiftUI. The benefits of using SwiftUI over UIKit are highlighted,
including its ease of use, more concise and declarative code, and better
support for live previews. The streamlined development process provided
by SwiftUI greatly aided in the implementation of frameworks such as
Swift Charts and WebKit. Overall, the use of modern technologies and
frameworks such as SwiftUI has greatly benefited the development of iOS
apps.

Body:

iOS app development is a complex weave of many different frameworks and
language constructs that are extremely uncommon in less modern
programming languages. This complex weave is what I am going to be
covering as I go over the different weave of technologies that I used in
the creation of the app GoDEX Pro over the course of this quarter. More
specifically I am going to cover how my use of the data driven SwiftUI
framework with Swift Charts and WebKit functionality worked together to
create a great resource for Pokémon go players around the world.

When trying to understand current iOS development practices it is also
crucial to understand how they got there. The history of iOS development
can be traced back to 2001 when Apple released their line of OS X
operating systems on Mac. These used the Cocoa UI framework
(FoundationKit and ApplicationKit) and the Objective-C programming
language as the basis for app development. In 2008, Apple opened the App
Store alongside the release of iPhone OS 2, opening up their mobile
platform for app developers using Cocoa Touch (FoundationKit and UIKit)
and Objective-C.

Fast forward to 2014 when Apple released a new programming language
called Swift. Swift was designed to be a modernized programming language
with many powerful built in features and programming paradigm changes.
Apple's UI frameworks (ApplicationKit, UIKit etc.) were updated to work
with Swift, but ultimately were still written in and intended for
Objective-C.

A few years later in March of 2019 Swift 5 was released, which has
developed a long way since Swift 1.0. It's ABI stable on Apple platforms
and has its own programming paradigms such as protocol-oriented
programming. Later in that year Apple announced SwiftUI at WWDC. SwiftUI
is a declarative programming framework for developing user interfaces
for iOS and macOS applications. With SwiftUI, Apple aims to update the
iOS development experience to the modern world by providing options
similar to other frameworks available at the time for web and Android
app development.

With the new paradigm shift that is SwiftUI, developers have much more
freedom over the way they can lay out objects. This new freedom comes
from the relative ease that SwifUI offers in implementing the dynamic
layouts that power many of the largest apps. It is also far easier to
read than most of the code written for UIKit which provides the added
benefit of easier to interpret code which is more readily iterated upon
in the future. This played a massive role in the creation of my app
GoDex Pro as I iterated through it over the course of the quarter. The
ease of changing elements with SwiftUI made tinkering with my project
far easier. The preview allowed me to see in real time exactly what the
view was going to look like before having to compile it which saved a
lot of time in the development process. What is almost certainly the
best part of SwiftUI in my opinion is how easy it is to at least mock up
a design in SwiftUI by just typing a few lines of code. This is due to a
combination of the features mentioned previously but also the fact that
there are no storyboards to lay things out manually on and connect them
to parts in the code.

The streamlined process that SwiftUI provides helps greatly when
implementing the different frameworks that it enables. Specifically it
helped when trying out the relatively new framework of Swift Charts.
Swift Charts is a framework which gives developers a super easy way to
visualize data. In my specific example Swift Charts allowed me to
visualize the statistics of different Pokémon compared what the average
of all Pokémon are. This will help users find which Pokémon are good at
different things, or at least understand why a specific Pokémon is used
often in the meta. In my specific project I only used a bar chart but
there are plenty of other charts that also do an excellent job at
visualizing different types of data.

SwiftUI also does an excellent job of making custom views far easier
such as is the case with my WebKit integration. I was able to make the
twitter page for Pokémon Go look like it was part of my app by simply
just including a view as part of my NavigationStack which displayed the
twitter page. With how easy it was to just do this it is no wonder why
every single web browser for iOS uses webKit.

Another thing that is helped by SwiftUI's super easy custom view making
was how easy it was to make a tab view work as an image cycler. By
simply just storing an array of strings which represent the names of the
images to display I can use a ForEach loop to iterate through the
different images and display what each Pokémon looks like in game, with
their event variations and shiny variations included.

In conclusion, iOS app development has come a long way since its
inception in 2001. The introduction of new technologies and frameworks
such as Swift and SwiftUI have greatly improved the development
experience for developers. The use of SwiftUI in the development of the
GoDex Pro app allowed for easy iteration and dynamic layouts, making it
easier to implement frameworks such as Swift Charts and WebKit. The ease
of creating custom views and the ability to preview changes in real-time
greatly streamlined the development process. Overall, the use of modern
technologies and frameworks such as SwiftUI has greatly benefited the
development of iOS apps, allowing for more efficient and effective
development.

Sources:

<https://www.hackingwithswift.com/interviews/ish-shabazz-what-are-the-advantages-of-swiftui-over-uikit>

<https://developer.apple.com/documentation/Charts>

<https://blog.logrocket.com/building-custom-charts-swiftui/>

<https://benoitpasquier.com/create-webview-in-swiftui/>

<https://medium.com/@deekshithbellare/what-is-abi-stability-and-why-does-it-matter-48c918554be1>

<https://medium.com/@rmeji1/declarative-and-imperative-programming-using-swiftui-and-uikit-c91f1f104252>
