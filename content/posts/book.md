+++
title = "My work in 2021-2022"
date = "2022-05-29"
author = "oddoz"
cover = "assets/img/book-cover.png"
description = "This article will be used as a \"book\" showing my work for my master degree's application."
+++

This article will be used as a "book" showing my work for my master degree's application.

## Diversifying my skills 

**2022: Trying to go Fullstack.**  

I chose to go this way because I like working close to the **products**. It allows me to have a **complete understanding** about how a web product or plateform is working. Also as I prefer beeing someone that can work on any web related topic than an expert in one field.  

#### What I got interested in

Let's do a quick review of my year as a student web developper.

It's been a amazing year of learning. On my free time and at work I learned completely new skills and technologies that I like. And I'm looking forward to be able to use those skills to create better and **more polished** school projects. Here's a quick list of my main interests this year: 

- Golang
- Cloud architecture through Google Cloud Platform
- Gunjs, IPFS, libp2p and decentralized stacks in general
- Godot Game Engine
- Fundamentals of Database enginering,
- SQL and Postgre

I also continue over the year to improve my Typescript and Nodejs skills and my overall computer science knowledge.

#### Apprenticeship

I'll start to talk about my apprenticeship and the work I realized here. I had a insane amount of work at this company. I joined Moneybounce because of the challenge there was. A friend of mine founded this company few years ago, he's also a student and I admire him a lot. By himself he manage to found a real brand and Fintech company when he was 19.

At the time we hadn't raise funds. I started by planning the next 4-5 months that will bring us to the Seed fund raising. With the other 2 developpers we managed to bring the product to something that could scale a little bit. At the time it was still clumsy and mostly a minimal viable product.

Thanks of the code we managed to write with a team of three 20 years old developpers plus the work that have been achieved by the whole team for almost 2 years, Alexis and Arthur managed to rise **$500k for Moneybounce**. 

After the funds raise we had the cash to hire a lead dev. Alexis and myself had to hire someone, it was a tought experience: finding amd hiring someone that should be way better than me and able to bring the team to the next step which is a fully automated and scalable product.

In the next section I'll talk about project that I worked on this year. Some Moneybounce related development will be mentioned here but I can't go to much in details on there as the developped tech and code base belongs to Moneybounce.

## Projects I worked on:

I will talk about 4 projects that I worked on. Most of my developing and coding time was while working on Moneybounce services so I can't show everything here. Here is 2 little side projects, 1 school project and 1 Moneybounce service.

#### Gokeep

Learning a language that runs at a lower level was something that interested me. At some point I wanted to start learning Go.  

**Gokeep** is a little password manager in terminal. It's currently archived because it was mostly a way of learning golang and I had others project to work on for school. But at some point I would like to come back at it and make it a complete local password manager that anyone could use.

Here's some screenshot of the Gokeep CLI in use: 

![GOKEEP MENU](/assets/img/gokeep2.png)

![GOKEEP MENU](/assets/img/gokeep1.png)

| Library & tools | Link                                              |
| :----:          |    :----:                                         |
| Cobra           | https://github.com/spf13/cobra                    |
| Sqlite Database | https://www.sqlite.org/index.html                 |

You can find the repository here: https://github.com/lafusew/gokeep.

#### Ants Simulation

At school we had a course on the Web Audio API & Canvas. For the exercice/little project we had to do I chose to build a Ants simulation. Following the same principle as [Pezza Work](https://www.youtube.com/watch?v=81GQNPJip2Y).

Let me quickly explain: Ant are using mainly **pheromones** to guide themself through their environment. I implemented a **pheromone system** where ants start by leaving their home, wondering around looking for food. At this point they drop pheromones that lead to their **home**. If they find found, they will try to **follow** their pheromones to get back to home while dropping **"to food"** pheromones. Other ants can now follow this pheromone's path and get to the food. 

![ANTS](/assets/img/ant3.png)

![ANTS](/assets/img/ant2.png)

![ANTS](/assets/img/ant1.png)


I really enjoy simulation where the **sum of basic & individual action creates a complex global system**. I also built a boids simulation that follow the same pattern.

You can find the repository here: https://github.com/lafusew/browser-ants-simulation.

#### Microservice PUB/SUB

During this section we're going to talk about microservice development and architecture at **Moneybounce**. First our Cloud architecture is located in EUW9 Servers of **Google Cloud platform** which are in **Paris**. 

We had to build a system that would continuously treats images before sending them to an external partner. We don't want our Client to be locked on waiting while services do their work. That's why we chose an **Event driven architecture design** using **Pub/Sub pattern** instead of the classic **Request/Response** that frontend developper usually deals with.

The image is uploaded from our client app to **Storage bucket**. I've configured this storage bucket to trigger a **Golang Google Cloud Function** when a new document is uploaded. This Cloud Function is a simple program written in Go that treat the image before uploading it to an other bucket where documents have already been processed. On this second bucket a Pub/Sub Subscription has been created that pushes documents metadata to our **App Engine** service that is responsible for the communication with the given external service, which this time is written in **Typescript** and running on **Nodejs**. 

For the client app, all you have to do is to **upload an image to a Cloud Storage bucket**. Then you don't have to worry for **reponses** from the differents services as they are **asychronous**. An **event** will be triggered **automatically** so, you can see on the app that your image has been completely processed and accepted.

#### Gobelins and 42 Gamejam: 2072

![2072 BTC Controller](/assets/img/btc_playtest.gif)

I joined the Vivatech gamejam that was in partnership with 42 for developpers and Gobelins for designers. I joined as a developper with 2 friends from 42's school. I already wrote an article about this gamejam that you can find [here](/posts/2072).


## What's next ?

This year I've shifted a lot from **creative development** to **backend and services development/design**. It doesn't mean that I want to leave Frontend development but I really wanted to be able to **handle both side of my projects**. Also I do like beeing the one that can link a fully visual and user focused experience with all the behind the scene services that are needed to have a **persistent** and **connected** experience. 

For the next year I would like to focus more on delivering fully fledge experience. For this year I focused on learning how thing should work and how I should **think about** them while **designing systems** that are working and scalable. During my master degree I would also like to cooperate with other developper that can handle the creativeness for me so we can build better/bigger products and experiences together. 

Also I would like focus more on **codebase scalability**. Because right now I still find that I'm having an hard time working on **bigger application** that needs to stay up to date and scale with the rest of services it is working with.

