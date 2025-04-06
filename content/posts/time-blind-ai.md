+++
date = '2025-04-05T15:00:56-04:00'
draft = false
title = 'Time Blind AI'

# Assign categories AI, technology, faith, pastoring, other
categories = ["AI"]
# Assign tags elevenlabs
tags = ["elevenlabs"]

+++

# The Curious Case of the Time-Blind AI: Lessons from Building an ElevenLabs Agent

Large language models (LLMs) are amazing, but they have a funny quirk: they don't really understand the passage of time within a conversation. This became super clear when we were developing an AI agent with ElevenLabs. You can learn more about their product here: [ElevenLabs conversational AI agents](https://elevenlabs.io/conversational-ai). I strongly suggest you check them out. It's a pretty amazing service. If you want to sign up, please use [this link](https://try.elevenlabs.io/davidwicks). It will give me a little kickback. In a nutshell, it's an LLM linked with a realistic chatbot. Amazingly realistic! I know it's not the same as a real person, but it can feel very, very real.

## The Challenge: Keeping Conversations on Track (and on Budget)

We wanted to create a system where people could pay a small fee to chat with an agent (or bot) about a specific topic. The problem? We needed to make sure the conversations didn't go on forever since we were paying by the minute. ElevenLabs charges per minute for their service. However, no matter what we tried, the agent just could not track the time correctly. If we told it to make sure conversations didn't go more than 12 minutes, sometimes it would go for 3, and sometimes it would go for 15. It was infuriating. I had wrongly assumed that it could keep track of time. It could not on its own! This is NOT intelligence. It is an LLM. I know LLMs feel like intelligence, but they are not!

## The Solution: Contextual Updates to the Rescue!

Our solution was to use contextual updates—something that, as of this week, is on the bleeding edge of what ElevenLabs offers. You can read about them here: [contextual updates](https://elevenlabs.io/docs/conversational-ai/customization/events/client-to-server-events#contextual-updates). Basically, it's a way to update the agent's creation prompt by injecting some new information. For our project, two minutes before the time was up, the AI would get a message saying, "Start the wrap-up sequence!" This is not seen or heard by the user, but it helps direct the conversation flow. In the agent's creation prompt, there is a specific set of instructions on how to end the conversation gracefully. Without this, the conversation would just abruptly end when the set time was up. This is not a very user-friendly or enjoyable experience. The way we have it set now, the conversation is drawn to a natural conclusion. It works like a charm! This was after months of trying to get the agents to track time. We tried using API calls to time servers, sending updated variable values to the agent, and more. These all "worked" but would sometimes cause errors or create pauses in the conversation, taking you out of the "real" experience.

What's cool is that contextual updates weren't available when we started. I'm not sure if they added it because of me, but I actually suggested it on their Discord server, and all of a sudden, it showed up! It was really neat to be part of developing something so cutting-edge.

## Diving Deeper: How Language Models Handle Time

Language models don't have a built-in sense of time. They process information based on the words and context you give them. This can lead to some interesting challenges when you're trying to build a real-time conversational AI.

For example, if you ask a language model about something that happened "yesterday," it will give you an answer based on what it knows about the day before. But if you keep talking for hours, and today passes into the next day, it won't automatically update its understanding of "yesterday" to reflect the new time. It's weird.

This is why we had to use contextual updates in our ElevenLabs agent. We needed to give the AI a little nudge to remind it that time was passing.

When I asked one of the AI agents how it understood time, it could only register the timestamps when it was actively speaking. If I waited five minutes to reply and then asked how much time had passed, it might say 1 or 2 seconds. I tried leaving it for an hour once, and it said 10 seconds had passed. This is because it doesn't understand the passage of time when there's no active conversation! Try it. Pick an LLM and have a conversation about how much time has passed. They have no idea! So we are a long way from intelligence. A "sense" of time is part of being conscious, isn't it?

## Why This Matters

This shows how important it is to remember that AIs don't experience time like we do. I think it also shows how much human understanding and insight is needed to make these systems work. We need to build systems to help them understand time's passage in order to have effective conversations and be useful tools. It also shows how AI is not as intelligent as we think. Don't be fooled. We are still needed!

## Side Note: The Importance of Tenacity

Throughout this process, I was reminded of the importance of being tenacious. There were many error codes, setbacks, and times when I had to start over. Before I understood that the agents didn't have an understanding of time, I just could not make sense of things. Unexpected things happened... then I thought it was working, but it was just a fluke. But I kept going, and eventually, we got it to work. This is the way developing things goes sometimes.

Let me know if you want to explore any of these topics in more detail: [contact](/contact/).