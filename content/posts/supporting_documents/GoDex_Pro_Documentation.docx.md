---
title: "GoDex Pro Documentation"
date: 2024-06-25T16:20:31-4:00
draft: false
---

Tyler Vergin

6/05/2023

CSC-391

{{< center >}}
Final Project Documentation
{{< /center >}}

My app is a continuation from my project from last quarter GoDex. My new
app GoDex Pro is designed to take all of the best things from the
previous app and make them both more usable and look better, as well as
add a few new features using SwiftUI. GoDex Pro is a Pokémon Go Pokédex
companion app that serves as a better version of the in-game Pokédex
which provides far more information. SwiftUI has made implementing a lot
of features far easier than it was using UIKit. The class diagram is
directly below this outlining the updated version of the app with the
screenshots below this that go over everything else.

{{< figure src="/images/GoDex_Pro_Documentation.docx/media/image1.png" caption="General UML Diagram of the system" align="center" >}}

{{< center >}}
{{< inTextImg url="/images/GoDex_Pro_Documentation.docx/media/image2.png" height="544" alt="A black screen with white text" >}}
{{< inTextImg url="/images/GoDex_Pro_Documentation.docx/media/image3.jpeg" height="543" alt="A screenshot of a phone" >}}
{{< /center >}}

These screens above are the loading screen that you see when you load the app
and will display until the API calls are made and the pokedex object is
fully instantiated with those API calls. The home screen is fairly
simple with just 2 links on it to both the pokedex view and the news
view in the top right corner.

{{< center >}}
{{< inTextImg url="/images/GoDex_Pro_Documentation.docx/media/image4.png" height="541" alt="A screenshot of a phone" >}}
{{< inTextImg url="/images/GoDex_Pro_Documentation.docx/media/image5.png" height="541" alt="A screenshot of a video game" >}}
{{< /center >}}

The screens above show the new news screen which displays all of the
latest community days and a link to a separate view which shows the
Pokémon Go twitter page. The Pokémon news screen just has a simple
LazyHStack which is horizontally scrollable and shows which Pokémon are
available during each community day, along with the date of the
community day. The twitter page is just a simple WebKit view which takes
a URL and displays the webpage from that URL, with the URL in this case
being the Pokémon Go news twitter.

{{< center >}}
{{< inTextImg url="/images/GoDex_Pro_Documentation.docx/media/image6.jpeg" height="543" alt="A screenshot of a video game" >}}
{{< inTextImg url="/images/GoDex_Pro_Documentation.docx/media/image7.png" height="542" alt="A screenshot of a video game" >}}
{{< /center >}}

These screens above are where most of the work has gone into. The Pokédex page
on the left has search functionality (which I forgot to include in the
screenshot but is in the demo video) and a LazyVGrid which displays all
of the Pokémon from the Pokédex. Each grid item is for a different
Pokémon and has 2 SFSymbols which when clicked will keep track of
whether the user has one (the left symbol that turns green) and whether
they have a shiny one (the one on the right which turns yellow).

The second screen is the detail view for the Pokémon. There is a TabView
which lets the user swipe through the different variants of the Pokémon
such as the shiny version and other event versions. The 2 SFSymbols
which keep track of if you've caught the Pokémon are also right next to
the elements with some statistics listed down below. The first card
shows the weight of the Pokémon, the ratio of which genders are more and
less common, as well as the height. The second card uses Swift Charts
which display the Pokémon's stats compared to the average of all Pokémon
stats.
