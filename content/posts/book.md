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

I chose to go this way because I like working close to the **products**. It allows me to have a **complete understanding** about how a web product or platform is working. Also, as I prefer being someone that can work on any web related topic than an expert in one field.    

#### What I got interested in

Let's do a quick review of my year as a student web developer.

It's been an amazing year of learning. In my free time and at work, I learned completely new skills and technologies that I like. And I'm looking forward to being able to use those skills to create better and **more polished** school projects. Here's a quick list of my main interests this year:

- Golang
- Cloud architecture through Google Cloud Platform
- Gunjs, IPFS, libp2p, and decentralized stacks in general
- Godot Game Engine
- Fundamentals of Database engineering,
- SQL and Postgre

I also continue over the year to improve my Typescript and Nodejs skills and my overall computer science knowledge.

#### Apprenticeship

I'll start to talk about my apprenticeship and the work I did here. I had a insane amount of work at this company. I joined Moneybounce because of the challenge. A friend of mine founded this company a few years ago. He's also a student, and I admire him a lot. By himself he managed to found a real brand and a Fintech company when he was 19.

At the time, we hadn't raised funds. I began by planning the next 4-5 months, which will lead to the seed fund raising. With the other 2 developpers we managed to bring the product to something that could scale a little bit. It was still clumsy and mostly a minimal viable product.  Alexis and Arthur were able to raise **$500,000** for Moneybounce thanks to the code we were able to write with a team of three 20-year-old developers, as well as the work done by the entire team over the course of almost two years.

After the funds raise we had the cash to hire a lead developer. Alexis and myself had to hire someone. It was a tough experience to find and hire someone that should be way better than me and able to bring the team to the next step, which is a fully automated and scalable product.

In the next section, I'll talk about projects that I worked on this year. Some Moneybounce related development will be mentioned here, but I can't go into too much detail on that as the developed tech and code base belong to Moneybounce.

## Projects I worked on:

I will talk about four projects that I worked on. Most of my development and coding time was while working on Moneybounce services, so I can't show everything here. Here are 2 little side projects; 1 school project and 1 Moneybounce service.

#### Gokeep

Learning a language that runs at a lower level was something that interested me. At some point, I wanted to start learning Go.

"Gokeep" is a little password manager in the terminal. It's currently archived because it was mostly a way of learning Golang and I had other projects to work on for school. But at some point, I would like to come back to it and make it a complete local password manager that anyone can use.

Here's some screenshots of the Gokeep CLI in use:

![GOKEEP MENU](/assets/img/gokeep2.png)

![GOKEEP MENU](/assets/img/gokeep1.png)

| Library & tools | Link                                              |
| :----:          |    :----:                                         |
| Cobra           | https://github.com/spf13/cobra                    |
| Sqlite Database | https://www.sqlite.org/index.html                 |

You can find the repository here: https://github.com/lafusew/gokeep.

#### Ants Simulation

At school we had a course on the Web Audio API & Canvas. For the exercice/little project we had to do I chose to build a Ants simulation. Following the same principle as [Pezza Work](https://www.youtube.com/watch?v=81GQNPJip2Y).

Ants primarily use pheromones to navigate their environment. I implemented a **pheromone system** where ants start by leaving their home, wondering around looking for food. At this point, they drop pheromones that lead to their "home". If they find food, they will try to return home by **following** their pheromones while dropping **"to food"** pheromones. Other ants can now follow this pheromone's path and get to the food.

![ANTS](/assets/img/ant3.png)

![ANTS](/assets/img/ant2.png)

![ANTS](/assets/img/ant1.png)


I really enjoy simulation where the **sum of basic & individual action creates a complex global system**. I also built a boids simulation that follow the same pattern.


| Library & tools | Link                                                     |
| :----:          |    :----:                                                |
| Canvas API      | https://developer.mozilla.org/fr/docs/Web/API/Canvas_API |

You can find the repository here: https://github.com/lafusew/browser-ants-simulation.

#### Microservice PUB/SUB

During this section, we're going to talk about microservice development and architecture at Moneybounce. First, our cloud architecture is housed on the **Google Cloud Platform** EUW9 Servers in **Paris**.

We had to build a system that would continuously treat images before sending them to an external partner. We don't want our clients to be locked in waiting while services do their work. That's why we chose an "Event-driven architecture design" using the **"Pub/Sub pattern"** instead of the classic **"Request/Response"** that front-end developers usually deal with.

The image is uploaded from our client app to the **storage bucket**. I've configured this storage bucket to trigger a "Golang Google Cloud Function" when a new document is uploaded. This Cloud Function is a simple program written in Go that treats the image before uploading it to another bucket where documents have already been processed. On this second bucket, a Pub/Sub Subscription has been created that pushes documents' metadata to our **App Engine** service that is responsible for the communication with the given external service, which this time is written in **Typescript** and running on **Nodejs**. 

For the client app, all you have to do is to upload an image to a **cloud storage bucket**. Because the services are **asychronous**, you don't have to worry about **responses** from them. An **event** will be triggered **automatically**, so you can see on the app that your image has been completely processed and accepted.

| Library & tools          | Link                               |
| :----:                   |    :----:                          |
| Google Cloud Pub Sub     | https://cloud.google.com/pubsub    |
| Google Cloud Storage     | https://cloud.google.com/storage   |
| Google Cloud Functions   | https://cloud.google.com/functions |


#### Gobelins and 42 Gamejam: 2072

![2072 BTC Controller](/assets/img/btc_playtest.gif)

I joined the Vivatech gamejam that was in partnership with 42 for developers and Gobelins for designers. I joined as a developer with 2 friends from 42's school. I already wrote an article about this gamejam that you can find [here](/posts/2072). In this article I explain in depth how we came up with this little game after 3days of work!

## What's next ?

This year I've shifted a lot from **creative development** to **backend and services development/design**. It doesn't mean I want to abandon frontend development entirely, but I do want to be able to **manage both sides of my projects**. Also, I do like being the one that can link a fully visual and user focused experience with all the behind the scenes services that are needed to have a **persistent** and **connected** experience.

For the next year, I would like to focus more on delivering a fully fledge experience. For this year, I focused on learning how things should work and how I should **think about** them while **designing systems** that are working and scalable. During my master's degree, I would also like to cooperate with other developers that can handle the creativity for me so we can build better/bigger products and experiences together.

Also, I would like to focus more on **codebase scalability**. Because right now I still find that I'm having a hard time working on **bigger application** that needs to stay up to date and scale with the rest of services it is working with.
