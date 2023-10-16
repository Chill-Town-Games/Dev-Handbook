# The Chilltown Dev Handbook
This is a general handbook on game dev as a community of volunteers and the common challenges and pitfalls.

## Introduction
This is a general handbook on game dev as a community of volunteers and the common challenges and pitfalls.
In game dev, throwing more devs and money at a project does not necessarily yield fun or good gameplay. It also doesn’t always make the development process faster. Notch made Minecraft Alpha alone. Stardew Valley also was made by a single dev. Cubeworld was made by a dude and his wife. Valheim only a team of 5. 
It’s a learning journey and the only requirements are being interested in this project and having the will to contribute. That’s it. 

## Common Pitfalls
- Game development is difficult, low paying and the public can be ungrateful and demanding. 
- It’s easy to get hyped and have a truck load of awesome ideas. Ideas are one thing, implementation is another. Think carefully before proposing features.
- Feature creep also leads to lots of shallow and useless items and features.
- Ambition is good but it’s mostly detrimental if the fundamentals aren’t even met such as making a fun game loop.
- Emotional attachment is a roadblock for making progress/optimization. Be ready to scrap features you spent hours working on.
- This community got a slight sigma grindset tilt which means burnout potential is high.
- Deadlines make games worse. Features should be released when they are finished. 
- Excessive process changes cause delays, deprecation and wasted time.

## Expectations
- This is all volunteer work so speed or consistency is not expected. With that said some degree of ownership is required (don’t just drop out without notice). 
- There’s no deadlines so no crunch. Don’t overwork yourself. If you need a time constraint to stay motivated, we can set time frames. 
- Don’t get overly hyped and emotionally attached. Work can get nuked if it doesn’t work out.
- Disagreements are bound to happen. They have to be solved with a consensus.
- Things may take 50% to 200% more time than expected to get working.
- Do not suffer in silence. Things might turn out to be trickier than initially thought. 

## Scope
- With the exception of major components such as the engine and networking, most if not all features should remain small. 
- Prefer refining existing features over adding new ones.
- If something takes too long to implement it will get dropped.
- Tasks should be manageable by 1 person but can seek help from anyone on the team

## Initial Feature wishlist
- Memorable soundtrack
- In-house engine
- Secondary build system for movable builds (to build things like trains and ships)
- Lua  scripting

## Workload distribution
- Tasks are gonna be organised using something like a collab todo board. 
- We will give job titles so every knows who does what based on existing or desired skill. 
- Tasks will be sorted into priority buckets.
- Tasks are assigned and owned by team members.
- If for whatever reason life gets in the way, let the team know. Nothing wrong with dropping out. 

## Standard procedure
- Use of git & github for all team members even non-technical staff
- Github for project management
- Systematic documentation
- Internal wiki 
- All text documents shall be written in Markdown
- Periodic check-ins to check for blockers


## Technicalities
- Vulkan rendering engine
- Lua scripting
- Engine modules and mods share the same architecture for easy integration
- Efficient chunk loading
- ECS engine
- No preemptive optimization before working prototype

## Short Term
- Player walk around
- Terrain
- Block placing

## Long Term
- Game rewrite for multiplayer
- Optimize for performance if required
- QA testing
- Listen to community proposal
