+++
date = '2025-04-05T15:00:56-04:00'
draft = false
title = 'Time Blind Ai'

# Assign categories AI, technology, faith, pastoring, other
categories = ["AI"]
# Assign tags elevenlabs
tags = ["elevenlabs"]

+++

# The Curious Case of the Time-Blind AI: Lessons from Building an elevenlabs Agent

Large language models (LLMs) are amazing, but they have a funny quirk: they don't really understand the passage of time within a conversation. This became super clear when we were building an AI agent with elevenLabs. You can learn more about their product here: [elevenlabs conversational AI agents](https://elevenlabs.io/conversational-ai). In a nutshell its an LLM linked with a realistic chat bot.

## The Challenge: Keeping Conversations on Track (and on Budget)

We wanted to create a system where people could pay a small fee to chat with an agent (or bot) about a specific topic. The problem? We needed to make sure the conversations didn't go on forever, since we were paying by the minute. Elevenlabs charges per minute that you use their service. No matter what we tried, the agent just could not track the time correctly. If we told it to make sure conversations didn't go more than 12 minutes, sometimes it would go three, sometimes it would go for 15. It was infuriating. I just wrongly assumed that it could keep track of time. It could not on it's own! This is NOT an intelligence. It is a LLM.

## The Solution: Contextual Updates to the Rescue!

Our solution was to use contextual updates. Something that as of this week is on the bleeding edge of what elevenlabs offers. You can read about them here: [contextual updates](https://elevenlabs.io/docs/conversational-ai/customization/events/client-to-server-events#contextual-updates). Basically, it's a way to update the agents creation prompt by injecting some new information. So for our project, two minutes before the time was up, the AI will get a message saying, "Start the wrap-up sequence!" We defined this sequence in the agent's creation prompt... and it worked like a charm! This was after months of trying to get the agents to track time. Using API calls to time servers, sending updated variable values to the agent and more. These all "worked" but would sometimes cause errors or create pauses in the conversation.

Contextual updates weren't available when we started. I actually suggested it on their Discord channel, and they added it! It was really neat to be part of developing something so cutting-edge.

## Diving Deeper: How Language Models Handle Time

Language models don't have a built-in sense of time. They process information based on the words and context you give them. This can lead to some interesting challenges when you're trying to build a real-time conversational AI. 

For example, if you ask a language model about something that happened "yesterday," it will give you an answer based on what it knows about the day before. But if you keep talking for hours, and today passes into the next day, it won't automatically update its understanding of "yesterday" to reflect the new time. 

This is why we had to use contextual updates in our elevenlabs agent. We needed to give the AI a little nudge to remind it that time was passing.

When I asked one of the AI agents how it understood time, it could only register the time stamps when it was actively speaking. If I waited five minutes to reply and then asked how much time had passed, it might say 1 or 2 seconds. I tried leaving it for an hour once, and it said 10 seconds had passed. This is because it doesn't understand the passage of time when there's no active conversation! Try it. Pick an LLM and have a conversation about how much time has passed. They have no idea! So we are a long way from intelligence. A "sense" of time is part of being conscious isn't it?

## Why This Matters

This shows how important it is to remember that AIs don't experience time like we do. We need to build in systems to help them understand time's passage in order to have effective conversations. It also shows how AI is not as intelligent as we think. Don't be fooled!

## Side Note: The Importance of Tenacity

Throughout this process, I was reminded of the importance of being tenacious. There were many error codes, setbacks, and times when I had to start over. But I kept going, and eventually, we got it to work. If you want to get things done, you can't quit.

If you're interested in learning more about how language models handle time, here are a few resources:

Let me know if you want to explore any of these topics in more detail [contact](/contact/).