# The Solution: Taming the Reference Copy Bug

Just by looking at the behavior of the app, I suspected a reference copy issue. The problem was that when we updated one verification, the changes propagated unexpectedly to others. This happened because the eligibility checks were being copied by reference rather than as separate entities.

To fix this, I used a deep copy method instead of a shallow one. By doing so, each verification and its associated checks became independent, preventing unintended side effects when toggling the values.

This approach ensures that the state is fully isolated, so each verification behaves as expected without interfering with others.

## Problem Provided

### How to run

* Clone the repo
 * Run `yarn` to install dependencies 
 * Run the server with `yarn dev`

### Challenge: Eligibility Check Chaos

This is a single-page application designed to test your debugging skills. You'll be presented with candidate verification based on eligibility checks from two different sources. Each source has four individual checks, and initially, one check from each source appears passed.

Here's the twist: when you try to toggle the other checks, things get strange. There seems to be a bug in the code causing unexpected behavior.

Your mission: dive into the code and uncover the culprit behind this bizarre behavior. Identify the bug and understand why the application reacts the way it does.

### Unveiling the Bug: The Key to the Fix

You've identified the weirdness in the eligibility checks, but don't just jump in with a fix! The real challenge lies in uncovering the root cause, the sneaky bug making things wonky.

Think like a code detective. Isolate the culprit, understand why it's causing trouble, and then propose a solution that sets things straight. This is how you'll truly showcase your debugging mastery!