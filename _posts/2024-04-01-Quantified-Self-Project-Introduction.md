---
layout: post
title: Quantified Self Project Introduction
description: Starting a personal data collection and analysis project
date: 2024-04-01T07:00:00-07:00
tags: Quantified-Self
---

## Quantified Self Introduction

### Premise

I watched a TED Talk recently called [*Own Your Body's Data*](https://www.youtube.com/watch?v=_GMVTJ9ZKVc). I highly recommend watching it for yourself. Talithia gives great examples of tracking personal data as a tool for taking ownership of your health. 

The idea of a personal database lived in my head for a couple months. I finally had a moment last week where I realized I was feeling stuck. I needed a project to work on, I wasn't keeping a consistent sleep schedule, I wasn't interested in going to the gym, and I just generally felt scattered and disinterested. I decided to take a walk outside; the fresh air and sun would make me feel better and clear my head so I could come up with an idea. The skeptic in me wondered &mdash; would spending a few minutes outside actually make me feel better? Could I just spend a while outside every day and guarantee I'd have more motivation to be productive? I didn't get an answer that day because those questions led me back to the idea of a personal database and back to the computer to get started. So in a sense, just thinking about going outside was good enough to get me started on a project.

### Questions

I started thinking about applications for my own personal database. I came up with a number of areas where I hope to gain insights from collecting my own data, and I'm sure I'll come up with more over time. I really like Talithia's personal health database. I've had questions about my own health and sleep quality, so this is a big one for me. I also like the idea of habit trackers. I always hear about the importance of good habits, but never built systems to support those habits. I hypothesize that building a habit tracker into my personal database will create a more powerful incentive to adhere to those habits. At the very least, I'll get some insight about my tendencies. 

Here are some of the topics and questions I want to explore:

- **Sleep**
    - How much sleep do I need? 
    - How well am I sleeping on a given night?
    - What does a solid sleep schedule do for me?
    - What happens when I introduce caffeine?
- **Behavior**
    - Can I create, reinforce, and measure impacts of my habits?
        - Time spent outdoors, workouts, productivity, reading, journaling, screen time, etc.
- **Mood**
    - What factors affect my mood? 
    - Can I create conditions that improve my general mood?
- **Health**
    - How do weight, temperature, heart rate, etc. change with my behaviors?
- **Environmental Factors**
    - How am I affected by weather, room temperature, air quality, etc.?

I think many people would put "Diet" somewhere in the list above, but I've tracked meals before and am not interested in doing that again at this time. I do have plenty of questions relating to my diet, so I'll consider adding it once I build out a better meal planning system for myself. For now, it would be too monumental a time commitment.


### Methodology


#### Behavioral Data Collection

I first put together a simple database from a template in Notion. I has checkboxes for a variety of habits, a couple of string fields for numerical data, and a multi-select for mood data. It adds an empty row each evening for me to fill in, but I have to remember to do so. In the meantime, I started brainstorming an extremely flexible app that would allow me to build out any type of habit tracker I wanted. Thankfully I didn't get too far down the Swift development rabbit hole before Googling my app concept.

I then found [Reflect](https://www.reddit.com/r/QuantifiedSelf/comments/179mlh0/reflect_ios_app_to_track_anything/), which does virtually everything I would have built into my app. I also found the [Quantified Self subreddit](https://www.reddit.com/r/QuantifiedSelf/), which is a community of folks conducting similar studies on themselves. The subreddit is not incredibly active, but it has good resources. Folks have posted incredibly detailed information about the results of their own experiments as well as reviews of things like tracking devices and supplements. I'll use the subreddit as a reference as I explore analyses and choose a daily wearable.

I'll be creating all my behavioral data collection forms in Reflect, which will make for relatively easy form modification and exporting. I'd like to automate as much as possible, but behavioral data likely needs to be self-reported for now.

I do have an idea for a device that lives on the bathroom counter and has a simple button and LED for certain behaviors that I want to track. I'm imagining a button for flossing, a button for taking vitamins, etc. At the end of the day, I'd push a "submit" button and it would update a database with that day's behaviors. It isn't a short-term goal but it would be an interesting little project.

#### Health Data Collection

I've wanted a wearable tracking device for a while now. I keep coming back to the Whoop and the Apple Watch. In an ideal world, I might have both. Realistically, there are pros and cons to each. The Apple Watch does more than simply health data collection, and it integrates with my iPhone very nicely. On the other hand, I already wear a watch so I'd have no use for my other watches. It's also quite expensive. The Whoop can be worn around the bicep and can be charged while it's worn. However, it has a subscription fee to access data, which is a huge turn-off for me. I'll probably end up with an Apple Watch at some point.

I also want to track other health metrics like weight and temperature. For now, these can be done manually. It would be fun to build a system that automates the data entry part of these measurements eventually as well.

#### Mood Data Collection

I read recently about workplace happiness and morale. The takeaway resonated with me. Work is not always, if ever, going to make me happy. Nor is it fair to expect life to always make me happy. A better metric to investigate is morale. Even if I have a bad day or rough patch, high morale will carry me forward. I am tailoring my mood-related questions to account for that.

#### Environmental Data Collection

The first environmental factor to track is weather. I think I'll probably just hit an API and grab the overall conditions and high temperature. I don't need a ton of detail here.

The second environmental variable is my actual ambient environment. I can buy a relatively cheap sensor that collects temperature, air quality, and humidity. I'm interested to see how my sleep quality correlates with my room temperature, among other relationships.





