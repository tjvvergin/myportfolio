---
title: "POGODEX proposal"
date: 2024-06-25T16:20:31-4:00
draft: false
---

Tyler Vergin

CSC 371 -- Final Project Proposal\
2/12/2023

Pokémon Go Ultimate Pokédex

The point of this app is to provide all the information about current
and future Pokémon Go Pokémon rotations, including but not limited to
which Pokémon are currently available in game, how they can be obtained,
maximum stats, and whether they are available in a shiny form all in one
place. It will also provide a way for the user to track their own
Pokédex entries so that instead of solely using the integrated Pokémon
go Pokédex they can use the one in app which will always remain fully
updated due to using the POGO Pokémon go API. This will fix the issue
inherent with the Pokémon go Pokédex where it will mark a Pokémon that
has not been released and therefore has never been available as part of
the Pokédex as simply not yet caught. This is something that greatly
confuses players and makes it extremely difficult to tell which Pokémon
they still need to catch, and which ones simply just have not yet been
added into the game yet.

I will be working on this project by myself and the resulting structure
of the app will end up being organized into at least these 4 screens,
with more possible screens to be added as necessary.

Screen 1: The main screen of the app, this will contain a list of the
other screens of the app

Screen 2: The profile section of the app which will let the user reset
their Pokédex entries

Screen 3: The main Pokédex screen which will have every Pokémon that
exists in the Pokémon universe, with the ones that aren't in Pokémon go
marked clearly as so, the ones that the player has not caught yet
unhighlighted, and the ones that the player does have with the
background highlighted. This page would be heavily assisted by the two
apis quartz 2d graphics and multi touch events. The user could select
multiple Pokémon at the same time to mark them as caught by first
initiating a 3d touch and then selecting as many as the user would like.
The actual UI on this screen would be made using the quartz 2d graphics
api.

Screen 4: This will be the more focused screen that displays each
Pokémon's more in depth stats, with the ability to mark each as caught
being on this page.

Full drawn out diagrams are provided in a pdf that has been submitted
along with this word file
