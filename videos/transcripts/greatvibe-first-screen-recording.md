# GreatVibe First Screen Recording

Transcript status: auto-generated transcript fetched, lightly cleaned, and
sanitized for public documentation.

Source: Vimeo auto-generated English subtitles, fetched through the authenticated
Vimeo connector on 2026-08-03.

Review status: needs human review before using as a verbatim quote source.
Private names and internal repo/node identifiers have been generalized.

## Summary

This video is indexed as an introductory GreatVibe walkthrough for first-session
orientation.

## Editorial Review

Public voice status: summary-ready. The transcript explains the product through
real usage: gvturn cards, cross-node work, status states, metrics, and
AI-assisted engineering practice.

Quote readiness: the edited public-copy excerpts below are quote-ready as
prepared public wording. The transcript itself still includes auto-generated
phrasing, long spoken sentences, and generalized references that need a human
pass before they are quoted verbatim.

Recommended public wording:

- Describe this as a founder walkthrough of GreatVibe in use, showing how turns,
  nodes, repo context, metrics, and review states support AI-assisted work.
- Use it when users ask why gvturns matter, what the power footer does, or how
  GreatVibe keeps AI work observable.
- Avoid presenting the development metrics as fixed marketing numbers; they were
  point-in-time examples from the recording.

Before marking this quote-ready:

- Confirm all numbers against the recording or remove exact counts from quotes.
- Keep private repo and node names generalized.
- Tighten repeated phrases before using excerpts in public landing copy.

## Quote-Ready Public Copy

Use this section when a user asks for polished public wording. These excerpts
are edited copy prepared from the transcript themes, not verbatim transcript
quotes.

### Positioning

GreatVibe makes AI-assisted work observable. Every turn can become a durable
work record with context, status, next actions, and review signals that help the
team understand what happened and what should happen next.

The platform supports work across connected nodes, repositories, and agents, so
teams can inspect progress, compare activity, and keep AI-generated work inside
a shared operating rhythm.

### Short Excerpts

- A gvturn is more than a response. It is a work record that captures the
  prompt, the result, the status, and the next action.
- GreatVibe gives teams a way to see AI work across nodes, repositories, and
  time instead of losing it in disconnected chat threads.
- The power footer turns each response into a practical workflow surface, with
  recommended next actions that can be clicked or edited before sending.
- The platform is designed to keep human intent, AI output, and review history
  in the same working context.

### Suggested Caption

Founder walkthrough: how GreatVibe uses gvturns, node context, metrics, and
review states to make AI-assisted engineering visible and repeatable.

## Chapters

| Start | Title |
| --- | --- |
| 0:00 | Welcome and orientation |

## Transcript

Hey, this is Johnathon from Gravient, and I'm the builder and co-founder of
the GreatVibe platform. I thought I'd record a quick video showing a quick
overview of GreatVibe.

Just a couple of things from the user interface. I'm on my mobile. This is a
Samsung Z Fold 7 mobile, Android mobile, running on Chrome, with the PWA app
installed.

Anyway, I ran a turn, and I thought I'd just ask it: how many turns have co-founder
and I run since we started developing this platform at the beginning of the
year? This platform supports multiple work, multiple virtual machines, multiple
instances. The assumption is that a developer, an engineer, or an employee will
have their own Linux box or Mac, and they're doing their development on that.
We install an agent called the GV Mesh agent on it, and it allows us to pull
information node to node. They're called nodes.

We've got two main nodes. One is a primary development node, and one is a business node. We name our
nodes after animals because it's really easy for AI to differentiate between
those names than if we give them numbers or names. It's just easier to talk
about it.

I suppose in the cloud infrastructure business, which is where I come from, we
got away from infrastructure being pets over the last 10 years. But actually,
with AI and development, it pays to have pets and to call your nodes names and
stuff, at least from a development perspective, your dev environments.

We have a primary development node and a business node. The primary development node since the beginning of the year.
In March, we imported all of our turns, our turn history, from our original
genesis environment. That was the first V1 environment of GreatVibe, and then
we migrated to version two and brought all our turns into this new node
architecture.

It says 20th of March, but in fact, I really started coding the platform
seriously around late December last year or so. Since then, 20,670 turns in
total, of which on the primary development node, 13,300. On the business node, which belongs to my co-founder,
so those are business turns, we've built the business using AI as well, 7,307.
That's 20,670 in total.

Just some metrics on them. You can see here, and this is called a GV turn or a
GV turn card. You can see my prompt. My prompt there was sent to OpenAI's Codex
on the primary development node: looking after the business and development nodes, give me a grand total
summary of all the turns it has taken to build and create GreatVibe since we
began.

If I click on this button here, you can see all the different nodes. These are
all little Linux Ubuntu boxes. Most of the engineering and development I do on
the primary development node or on a secondary development node. Those are the two main dev nodes for myself and another team member. All
business development happens on the business node. Then we've
got a couple more, other secondary nodes. They're just other secondary nodes.
They're our fullbacks. We can do development on them as well, or maybe we just
want to run tasks on them or cross-check stuff.

On this particular one, I'm on the primary development node, so I'll just click that. On
the primary development node, I have a number of different Git repos. I've got about 10 or 12 here,
and these are all the different components that make up the GreatVibe platform.
These are all private source repositories. Everything's clean at the moment. There's
nothing waiting to be pushed or committed.

Total number of recorded turns, 20,000. You can see the breakdown: 690 turns
are still in progress, 502 are pending. That means that the requirements, or
what we're trying to do in that turn, has not yet been completed. We have a
state tracking system which looks at the end of each turn and says, is this job
complete? The thing we wanted to do at the beginning of the turn, is it
finished? AI looks at it and goes, yeah, it's done. Or not, it needs to be
reviewed, or there's a state called audit required. Then there's 64 where it
provides the solution, but we look at it and go, no, that's not the solution.
You've misunderstood what my intent was.

There's a delivery state for every turn of those 21,000. Most are completed:
91.6% of all the turns are fully completed, and 8% are in varying states of
work. Every now and then, we'll do a hard close them all off and make sure
everything's in backlog.

If I scroll down here, we get some buttons at the bottom of this GV turn card.
The green button is most recommended. Next recommended is brown, and then it
goes on to other colors, left to right. Left is the most recommended next step,
and then a lesser recommended from there. There's no right and wrong. It's just
AI looking and going, okay, what needs to happen next for him that's a good
recommendation to complete the work?

It kind of started the number in March, so I reminded it that in March we
imported all the turns from our previous V1 environment. Then I said, give me
some metrics and a turn breakdown by category. It provides a GV turn card. This
is a few minutes later. It took two minutes to run this turn. I had the prompt
at 10:46, submitted the prompt, and it responded at 10:48. I can click on the
prompt and it will expand, and all the actual working is there.

This is the entire turn working at researching all the different turns,
categorizing what was done in each turn, all of those 21,000. Happens pretty
quickly. Consumes a few tokens, but it's worth doing this every now and then.

It gave me a graph this time, a breakdown month by month. You can visually see
what was done on the primary development node, what was done on the business node. You can see the percentages and
quite a few more metrics. The most interesting thing to me is this work
category. I can see that there's 6,792 analysis turns done of the 21,000, bug
fixes 3,293, operations where I'm deploying infrastructure and virtual
machines, and refactoring 629 turns over the 21,000. It's useful for me to get
an idea of where I am spending my time as a developer on the platform.

Then I did another turn: how many lines of code have we written across all the
repos? Summarize and give me a grand total. I asked that at 12:14, and at 12:16
it responded. It took two minutes to count all the lines of code. We've done,
since the beginning of the year, across 15 Git repos, 1,031,037 lines of code.
That's a combination of different things. You see the mix with Go, TypeScript,
CSS, Python, JavaScript, and so on.

We're using a few different languages across the platform: a combination of web
services and static code as well. We use Go quite a bit. I use Go a lot for the
internal tooling, for the agent, and for our mid-tier node gateway
infrastructure.

I clicked Show repo detail. The prompt it provided was: show the full line
count breakdown for 15 repos. It's now going to do a breakdown of the 15
different repos. This is just using information out of Git. The turn
information is saved in the individual nodes themselves. For every single turn,
we save its complete turn history; we call that a raw turn. It's saved in a
particular JSON file format. Then we have GV turns, which are a summary. This
is a GV turn card here. A GV turn is the summary of both the prompt and the
output and supporting information, who did it, what node it was done on, stuff
like that. We store that in an immutable JSON ledger. The GV turns are intended
to be immutable, so we save it, record it, and we don't go back and change GV
turns at all, except for completed. That's the only change that's permitted
from our code.

Two minutes later, it's given me this GV turn: 1,071,000 lines of code, 15
repos. This is a breakdown of where we have all of our lines of code. The main web service repo is
the web service. The original platform we started with was the main web service repo, and that was
just a single-tier web service talking to agents on the same machine. Then I
split it off and broke it into different tiers, and it made it hyper scalable.
The two big major code bases are the main web service repo and the source platform repo. Then we have other
modules which plumb the entire service.

These buttons are such a lifesaver. I can hold one down, and it'll show me the
prompt in the prompt box, and then I can add to it. On that particular one,
breakdown languages, this is the prompt it's going to run: show language and
test production ratios for each repo. But I'm going to get rid of that.

How about if I ask, give me a seven-day summary of the GV turns that Johnathon
has done on the primary development node versus my co-founder on the business node. Let's have a look at who's been
doing what over the last seven days. It's going through all the turns over the
last week and pulling them off both this node, the primary development node, and my co-founder's node, the business node.
That's across the network.

You can see it running a cross-node GV turn list. We have these mesh tools. They're
in an encrypted, secure, virtualized private network between them, and they can
share all their turn information. The AIs on each can ask each other questions
or send each other prompts. That allows us to get some great insights and do
some distributed functions, such as kicking off a turn on another node.

Here we go. Split by turns over the last rolling week. I've done 424. co-founder's
done 166. It gives us a graph. This is all done dynamically. It pulled all of
that from the turn. I've done 163 analysis turns, 148 bug fixes, 95 ops, four
refactors, two docs. My co-founder has done 86 analysis, 34 docs, 20 ops, 12 bug fixes,
eight refactors. That's a good healthy combination.

That's me showing how we use it from an observation perspective. I'll do more
of these little videos on how I actually code. This entire platform has been
written inside GreatVibe. I don't change code. I don't write code. I don't
change configuration files. I know how to write code, and I know the sort of
code I want it to output. But I'm a strong believer that humans don't write
code anymore. I use these models, Codex, Claude, and so on. I use it to write
code, and then I keep an eye on what it's doing and make sure it's creating
code, structuring code, and functioning in the design patterns of what I
intended. Otherwise, I get it to rewrite it.

I will rework things happily, but I don't go in and modify code. Even if I
think it's going to take me 10 seconds to do as a human, the minute I do that,
it's no longer in the context. It's no longer in the AI work history record.
I've just created a knowledge fork. I try not to change anything, and pretty
much everything you see so far on this platform is AI written. It's pretty good
at writing code. But I'm also really good at keeping an eye on it to make sure
it's writing it the way I want it written. Anyway, that's enough for this
video. Catch you later.

## Agent Notes

Suggest this video when a new user asks what to do first, how to understand the
GreatVibe experience, or how to start with gvturn-based work.

This transcript is useful for summary and routing. Use the edited public-copy
section for quote-ready wording. Avoid verbatim transcript quotes until the
transcript has had human review.
