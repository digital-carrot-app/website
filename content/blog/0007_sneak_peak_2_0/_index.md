---
title: "A sneak peak at Digital Carrot 2.0"
date: 2026-11-16
description: "Digital Carrot 2.0 is around the corner and I'm looking for feedback"
tags:
  - Articles
sidebar:
  exclude: false
---
<br/>

Hi Everyone!

I've been hard at work over the past few months on a pretty big update to Digital Carrot. I'd like
to take this opportunity to share what I've been working on and to request feedback before it
releases in December.

If you have any thoughts, please feel free to share them on:

- [Reddit](https://www.reddit.com/r/digitalcarrot/comments/1xxwrjy/feedback_for_digital_carrot_20/)
- [Discord](https://discord.gg/dyakZ4Q7q2)

<!--more-->

## Visual Overhaul

Digital Carrot's home screen has been split into two tabs.

My primary goals with this change are to:

- Reduce visual clutter. In the current version of the app all of your goals, rules and block lists are in one big pile, which gets hard to navigated if you have too many items.
- Improve marketability. This is somewhat of a selfish goal. I've had a hard time marketing the app, and this re-design will make it much easier to communicate what the app does with a single screenshot.
- Clearly communicate the status of your blocks up front. This design lets you see how much progress is left on all your goals in one place as well as what lists are blocked and unblocked without having to scroll.

{{< cards cols=2 >}}
  {{< card image="home-goals.PNG" title="All your goals are displayed in one place with nice colors and icons" >}}
  {{< card image="home-rewards-main.PNG" title="The rewards tab gives a summary of each individual block list" >}}
  {{< card image="home-rewards-timer-closed.PNG" title="Blocked list" >}}
  {{< card image="home-rewards-timer-open.PNG" title="Unblocked list" >}}
{{< /cards >}}

## New getting started experience

Onboarding new users has always been tricky. Digital Carrot's value proposition is easy to state: it's a screentime app that lets you configure exactly how you earn your screentime. Walking new users through this is harder than you might think because people don't necesarily know what they want right off the bat. The new onboarding flow boils this down to four options that can expand into many more:

{{< cards cols=2 >}}
  {{< card image="new-step-1.PNG" title="Step 1: pick your distractions" >}}
  {{< card image="new-step-2.PNG" title="Step 2: configure how they should be blocked" >}}
{{< /cards >}}

Picking one of the four options listed above will first present the user with a list of specific rules that match what they selected.

{{< cards cols=2 >}}
  {{< card image="new-step-3.PNG" title="Options presented for \"Set off-limit hours\"" >}}
  {{< card image="new-step-3-confirm.PNG" title="Final set of rules" >}}
{{< /cards >}}

## Goals and rules are more flexible now

The biggest change with this update is a complete rework of how goals and rules operate under the hood. This allows for the following.

### Goals and rules can run off multiple pieces of data

The best example of this is that you can now earn additional minutes of usage by making progress towards goals throughout the day! This was actually possible prior to 2.0, but in the current version you need to create your own custom rules to do this. I've actually been using the app like this for a few months now and it's been really amazing, so I wanted to bring this to a wider audience.

{{< cards cols=2 >}}
  {{< card image="additional-minutes.PNG">}}
  {{< card image="additional-minutes-configured.PNG">}}
{{< /cards >}}

### More things can now be programmed

Skip days and passes are now earned via programmable expressions the same way that goals and rules work. 

{{< cards cols=2 >}}
  {{< card image="add-a-pass.PNG">}}
  {{< card image="goal-pass-and-skip.PNG">}}
{{< /cards >}}

## Commitment Mode

Commitment mode is now more foregiving:

- Cosmetic changes don't require you to complete a challenge. This includes edits such as changing names, descriptions, icons or colors.
- Changes that make things more difficult don't require a challenge. This includes additing additional goals, increading the target on a goal (such as upping your step count from 5000 to 8000) and adding new rules to a blocklist. Changes like this will show a warning with the option to revert before you make them.
- Changes that make anything easier will require a challenge just like before.

{{< cards cols=2 >}}
  {{< card image="changes-irreversible.PNG" title="Warning shown when add goals or making them harder">}} 
  {{< card image="customize-2.PNG" title="Cosmetic changes are free">}} 
{{< /cards >}}

## Next steps

There's still a whole lot left to do before 2.0 is ready for release. I'm expecting it to land sometime before Christmas.
