+++
date = '2026-08-23T14:31:00Z'
draft = true
title = 'Pain-driven development is not always wrong'
author = 'Jon Abbott'
description = 'Pain-driven development is an informal pattern, not a methodology. A look at when waiting for real friction beats speculative engineering.'
tags = ['software engineering', 'pragmatism', 'coding patterns', 'architecture', 'technical debt']
+++

Pain-driven development, or PDD, is an informal, tongue-in-cheek term for a way of working where change only happens when something hurts enough. It’s not a formal methodology like Test-Driven Development or Domain-Driven Design. It’s more of a pattern you notice in teams and codebases.

It sounds irresponsible. Sometimes it is. But it’s not always wrong.

## What pain-driven development actually is

You see it when refactoring only happens after a messy release.
When tests appear after a nasty regression.
When monitoring is added after a late night incident.

That’s PDD in practice. Change follows discomfort, not a roadmap.

It’s easy to dismiss. Waiting for pain before you act can look like neglect. And sometimes it is. But there’s another reading: waiting for real friction before you invest in the wrong abstraction.

## The problem with chasing principles too early

Most engineers know the classics:

- SOLID
- Don't Repeat Yourself
- You Aren't Gonna Need It
- KISS principle

They’re useful. They exist for good reasons. They help us manage change.

But they’re heuristics, not laws.

When applied too early, or too rigidly, they create a different kind of pain. Not runtime failures. Design theatre.

You end up with:

- Interfaces for a single implementation
- Abstractions that hide nothing
- Configuration layers for behaviour that never changes
- Generic solutions to problems you might never have

That’s not good engineering. It’s speculative engineering.

PDD pushes back against that instinct.

## Pain reveals real problems

There’s something honest about waiting for friction.

Pain has a way of exposing what actually matters. Not what might matter someday. What’s actually in the way right now.

Here are three examples.

### Duplication that isn’t really duplication

A team builds two endpoints that look similar. The validation logic overlaps. Someone suggests extracting a shared service to keep things DRY.

They wait.

Three months later, the business rules diverge. One endpoint adds new constraints. The other changes its workflow entirely.

If they’d forced Don't Repeat Yourself too early, they’d now be unpicking a shared abstraction that no longer fits.

By tolerating a small amount of duplication, they avoided locking in the wrong model.

That’s pain avoided by accepting a little imperfection.

### The interface that never needed to exist

A new payment provider integration is added. There’s only one provider. The team debates introducing an interface and multiple implementations to follow SOLID, specifically dependency inversion.

They decide not to.

A year passes. The provider never changes. No second provider appears.

The simple concrete class was enough.

Had they introduced abstraction early, they’d have paid an ongoing complexity cost for flexibility they never used.

PDD in this case meant waiting for actual variation before generalising.

### Testing where it hurts

A legacy reporting module has almost no automated tests. It works, mostly. It’s ugly, but stable.

Rewriting it for purity would take weeks.

Instead, the team adds tests only around the parts they actively change. Each time a bug appears, they lock it down with a new test.

Over time, the high-risk areas become well covered. The stable areas remain untouched.

It’s not clean. It’s not textbook. But it’s focused.

Pain guided the investment.

## Principles work best when anchored to experience

The danger isn’t the principles themselves. The danger is applying them without context.

SOLID makes more sense after you’ve felt the pain of tight coupling.
Don't Repeat Yourself becomes real after you fix the same bug in five places.
You Aren't Gonna Need It feels obvious after building a framework nobody used.
KISS principle lands properly once you’ve wrestled with accidental complexity.

Pain turns abstract rules into practical judgement.

Without that experience, principles can become cargo cult practices. Followed because they sound right, not because they solve a real problem.

## The difference between reactive and reckless

Defending PDD isn’t the same as defending neglect.

There’s a difference between:

- Ignoring clear warning signs
- And waiting for meaningful signals

If change is frequent and risky, invest early.
If duplication is spreading and already diverging, extract.
If coupling is blocking delivery, refactor.

But if something is stable, rarely touched, and easy to understand, forcing it into a "clean" architecture might create more problems than it solves.

The key question isn’t "Does this follow SOLID?"

It’s "Where will this hurt if we leave it like this?"

## Pain as a prioritisation tool

Time is finite. Attention is limited. Not every imperfection deserves immediate correction.

PDD, at its best, acts as a prioritisation filter.

It asks:

- What’s actually slowing us down?
- What’s causing real defects?
- What’s stressing the team?
- What’s blocking change?

Fix those first.
Leave the rest alone until it earns your attention.

That doesn’t mean you never refactor. It means you refactor with purpose.

## A balanced view

The goal isn’t to live in constant firefighting. Chronic pain leads to burnout and brittle systems.

But eliminating all discomfort isn’t realistic either. Some friction is the price of moving fast.

Healthy teams sit somewhere in the middle:

- They don’t chase purity for its own sake.
- They don’t ignore obvious design debt.
- They let real problems shape their architecture.
- They use principles as tools, not trophies.

Pain-driven development sounds like a criticism.
Sometimes it is.
Other times, it’s just pragmatism with better timing.

And in a world full of over-engineered systems, a little well-timed pain can be surprisingly clarifying.
