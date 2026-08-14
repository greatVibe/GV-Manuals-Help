# Johnathon Intro to GreatVibe — transcript

- **Video:** Vimeo 1217843223
- **Duration:** 26:07
- **Published:** 2026-08-14
- **Caption source:** Vimeo English auto-generated captions
- **Transcript status:** Machine-generated, lightly normalized for GreatVibe product names; review against the recording before using exact quotations.

## Chapters

- 00:00 — Welcome and the GreatVibe premise
- 00:38 — AI-centric coding and directed collaboration
- 02:49 — Nodes, gvmesh, gvsandbox, Claude, and Codex
- 04:18 — GreatVibe building and operating itself
- 10:23 — Mochi, public manuals, and getting started
- 11:32 — Sending the first prompt
- 13:12 — gvturn cards and follow-up choices
- 15:19 — Audits, model switching, and review
- 17:26 — Git, credentials, settings, and files
- 19:17 — Meshes, organizations, and collaboration
- 22:16 — Cloning repositories and the Files explorer
- 24:18 — Secrets Vault and the trust chain
- 26:00 — Closing

## Transcript

[00:01] Hi, welcome to GreatVibe. I'm Jonathan Mastri, the co-founder

[00:07] and builder behind GreatVibe. I started building this platform late last year,

[00:13] seriously from about December,

[00:16] late December

[00:18] in 2025. So, welcome to the platform. We hope you enjoy it.

[00:24] Thanks for taking the time to take a look at it.

[00:27] In this video, I'm just going to share some information,

[00:31] some of the thinking and logic behind the platform, and also give you some pointers

[00:35] on where to start.

[00:38] GreatVibe is a coding platform, an AI-centric coding platform.

[00:45] I wouldn't say it's AI-assisted. I would say we

[00:51] treat AI as a kind of first-class partner in the process, and you'll see that plays

[00:57] out in the architecture behind it.

[00:58] And by that, I mean

[01:01] we

[01:03] give AI the tools and knowledge, and information it needs to make good choices or

[01:09] good recommendations to us. This is designed for not just your

[01:15] test projects or samples or playing around or prototyping, but it's also designed

[01:20] for developing and building complex software, complex business applications.

[01:25] The stuff we work with every day.

[01:28] And as a result, it's not a simple platform. It is complex.

[01:33] We work with a lot of different tools, languages, architectures, infrastructure.

[01:39] Everything is multi-tier in our modern world.

[01:43] Everything has a component that's web-based.

[01:46] This is a very Linux-centric development environment at the moment.

[01:51] You'll see that as a real strong part of its heritage.

[01:54] It's a part of where I come from, spending most of my career working with

[01:59] Linux-based technologies and web services architectures.

[02:05] And so look, it's not trivial. It's complex.

[02:08] There's a bit to learn,

[02:10] but it's super powerful. But it's also additive.

[02:14] So we take all the great features and incredible capabilities of

[02:19] the frontier models from Anthropic and OpenAI, and we build on top of it.

[02:23] We build on top of it in ways that, as a developer of

[02:29] production

[02:31] applications and production environments, that it's

[02:37] easier for you to control and build and design and also critique and

[02:43] audit your capabilities. So, with that in mind, let me share

[02:49] some kind of key concepts for GreatVibe.

[02:53] First is this is Linux-based.

[02:57] It's the agent. So we have an agent architecture.

[03:01] We have a couple of tiers of infrastructure on the GreatVibe

[03:07] side. So, in our data centers.

[03:11] And then on Linux nodes or macOS nodes, workstations,

[03:17] virtual machines, you can install an agent, and the agent is called gvmesh for

[03:23] GreatVibe Mesh. And you have our agent, our gvmesh agent,

[03:29] you install on a Linux virtual machine, so whether that's one of ours that we

[03:34] provide or your own. And from there, it'll automatically

[03:39] install agents for Claude and Codex, the latest versions.

[03:44] It runs in a sandbox environment called gvsandbox.

[03:47] And from there it's

[03:50] functioning

[03:52] down at the OS level exactly like Codex and Claude do.

[03:58] And that is because we absolutely love Codex and Claude.

[04:02] We don't want to be a replacement for them.

[04:04] We want to leverage all their incredible capabilities, but help you do it in a

[04:08] controlled manner, help you do it in a

[04:12] premeditated manner.

[04:15] And an example of that is GreatVibe itself.

[04:18] So we've built this entire platform from the ground up using GreatVibe.

[04:24] So it's built with itself. In the really early days, in late December, I had an

[04:29] initial kind of bootstrap version. It was really basic.

[04:32] It was incredibly basic, but it got to the point where I could enter prompts in it

[04:35] really quickly. And then since then, everything's been built inside GreatVibe.

[04:40] So it's been coding itself, and we still do it now.

[04:42] I use GreatVibe to keep developing the platform now.

[04:45] I also use it to run everything, run all our operations, running all of our

[04:49] production infrastructure and non-prod infrastructure.

[04:54] So that's important. That's a real distinction.

[04:57] But with that, we don't change anything outside of

[05:03] by hand. We're not saying that you will do the same thing, but I don't change

[05:08] config files, I don't change code, don't change documentation.

[05:11] I do everything through AI, and I do that for a couple of reasons.

[05:17] The first reason is, I obviously want to push it to its limits.

[05:22] I wanted to see when I started this, how far could I go?

[05:25] I wanted a tool that basically replaced my entire development and operations

[05:30] environment. And that's what I wanted GreatVibe to be.

[05:36] So to get there, I've had to use it for everything, because then I quickly learned

[05:40] its limitations, learned where I need to build some capability into GreatVibe

[05:45] versus what comes from OpenAI or Anthropic.

[05:49] That's the first reason. The next reason is I wanted an entire history, and

[05:55] we have an entire history now of every turn, every change, everything that's gone

[06:01] on to build the entire company. So there's myself and David that founded Great

[06:06] Vibe. I build all the technology, all the platform. I am the main builder.

[06:11] David's built our business using GreatVibe.

[06:16] So we haven't built any system, any document, any website, nothing at all outside

[06:22] of GreatVibe. Everything we do is done inside of GreatVibe.

[06:25] And that kind of alludes to our future direction where we want to take this

[06:31] platform. But GreatVibe it's built the business as well as the technology behind

[06:36] the business. We use it to stand up every system.

[06:39] And an example is all the operations platforms.

[06:43] So this is our production customer-facing environment, the environments you use.

[06:48] Behind the scenes, we have our dashboards, our command and control center, our

[06:54] monitoring, all of that tooling, every single thing we use has been built by Great

[06:59] Vibe. So we're constantly

[07:05] not only developing the platform itself, but seeing the best way to use it to build

[07:11] our own business, to build our own tooling.

[07:14] And that kind of also alludes to that everything we run

[07:19] is built with GreatVibe. And it's really

[07:25] only the CLIs from Claude and Codex,

[07:30] and a few other kind of tools internally, but pretty much everything,

[07:36] everything we do has been built with GreatVibe.

[07:39] And we run everything on AWS, Amazon Web Services.

[07:44] All of our Amazon infrastructure has all been designed and deployed by GreatVibe.

[07:50] In the early days, I gave it an account, an administrative account,

[07:56] an early version of GreatVibe, and then we did a number of turns to design all the

[08:00] infrastructure, design the platform.

[08:02] So we don't just write the code, we design the infrastructure and the platform it's

[08:05] going to run on. And we do lots of turns looking at different scenarios.

[08:09] Okay, so if we have this particular server architecture with this particular client

[08:14] architecture, what sort of service infrastructure, load balancers, DNS,

[08:19] security groups, what are all the different things we need on AWS?

[08:22] And so in the early days, I gave an account, and I haven't configured anything on

[08:27] AWS or any of our other infrastructure. I haven't configured anything at all.

[08:31] Everything's done through a turn.

[08:32] So now in August 2026, we're at around about roughly, I

[08:38] think, 23,000 turns. And I know some of those turns, there'll be thousands there

[08:44] that are just trivial, which you'll think, "My gosh, why didn't you just log into

[08:46] AWS console, change it? Why don't you just go and change that TypeScript source

[08:51] file or what have you?" But we have a history now, and we can look back and I

[08:57] can

[08:58] do a turn and go do, get a full analysis on any type of operation

[09:04] we did. And that's really super powerful.

[09:07] So we're not just doing--

[09:10] An example is your Git history.

[09:13] So yeah, it's great to have good Git commit history, and AI helps with your commit

[09:18] history. There's nothing like not having to type in explanations in your commits,

[09:25] and the models do that for me. But richer than that is,

[09:32] what did I do in that turn to come up with that code and logic?

[09:34] We can go back to every turn and say, "Hey, for this particular file, what was the

[09:39] thinking there?" And we've got what we call the raw log of every single turn.

[09:46] And it's a pretty big repo now. It's not massive.

[09:49] I mean, it's all just text, right? And it's all JSON at that, but super powerful

[09:54] because now we can look back at previous decisions.

[09:57] We can look at what the model was thinking back then.

[09:59] We can look at the AI assistant output at the time of what its thinking was,

[10:04] and then we can compare it to what AI thinks now.

[10:08] And of course, that's been an evolving situation.

[10:10] So

[10:12] now, before this video drags on too long, it's been 10 minutes already, and David

[10:17] gave me instructions to do a two-minute kind of intro video.

[10:20] Let me just give you some quick pointers before you get started.

[10:23] First of all, you're on a node called Mochi, and Mochi's our beginner node.

[10:28] It's our GreatVibe node. It's our way to give you documentation.

[10:31] It's kind of like a playpen. It's in a sandbox of its own.

[10:35] You can't see anything else. You can't connect to anything else from it.

[10:38] You can't get to it on the open internet, et cetera.

[10:41] It is a tiny little Linux machine.

[10:45] At the moment, it's running the Claude CLI.

[10:49] We do have plans to have the Codex CLI on it, so maybe by the time you see this

[10:53] video, Codex is there as well. It's got free access using Claude.

[10:59] It's absolutely tiny. It's got not a lot of RAM.

[11:03] You won't be able to code on it. You'll be able to do turns and questions and Q&A

[11:08] and ask about the documentation. And it'll be your go-to place to kind of see

[11:12] information, documentation, manuals, and stuff for us, and we'll be pushing out

[11:15] updates to the Git repo on it that's called gv-manuals-help.

[11:21] And that's our

[11:24] public repo of documentation and information you should know about the platform.

[11:28] So that's where you've landed now. You've landed in the Mochi node.

[11:32] You can just type in a turn, type in a prompt down below, ask it a question about

[11:37] anything, and then hit send, and you'll see how a turn works.

[11:42] And that's where things start to look a little bit different.

[11:45] We've tried to give you really rich insight into what's going on.

[11:49] You'll want it as a developer. If you are a professional developer,

[11:57] we don't make assumptions on our code, right? We check and verify.

[12:01] So you're going to want to watch your turns. I know I do.

[12:04] There's lots of turns, even though we're 23,000 turns in, I watch most of my turns.

[12:10] There's a few where I'm really confident it's not going to go sideways or implement

[12:15] things I can't quickly verify. But a lot of my turns are,

[12:21] they're changing code that's really important to me, or functions or parts of the

[12:24] stack that are really important. And so I watch a lot of the turns.

[12:28] I don't type on them. I do the work. I do the work from my perspective as a

[12:34] controller, and a verifier,

[12:38] an engineering manager, treating my AI agents as first-class citizens.

[12:43] I let them do their job, but I first of all make sure they've got good information

[12:47] to begin with, and then I verify afterwards what they did.

[12:51] And I may use them to verify themselves and the work they did, or I may use one of

[12:56] the other models. I may switch over from Claude to Codex, Codex to Claude, et

[12:59] cetera. So, you're on the Mochi node. You can run some turns.

[13:03] Type in a prompt now, hit send, and then you'll see the turn work, you'll see the

[13:06] tool calls. You'll see any AI assistant text where AI's talking during the turn.

[13:12] And also then at the end, you'll see what we call a GV turn card, so a GreatVibe

[13:17] turn. And this is like taking all the information in the turn,

[13:23] and telling the AI to give us HTML output, a rich HTML output,

[13:30] with some options of what to do next based on the turn we just did and the last

[13:34] previous turn. So in every turn, we feed in the last few turns, or we feed in

[13:38] pointers to it because most of it'll be cached.

[13:42] We feed in pointers to the last few turns, so it's got some turn history.

[13:45] And then when at the end of the GV turn card, you'll see it, and if you look on

[13:49] your screen now, you'll see that there's some buttons there.

[13:51] There's what we call the choice buttons.

[13:54] Everything you see in the GV turn is decided and chosen by AI.

[14:01] I've got a really strong engine there, a controlling and directing engine.

[14:06] But we don't

[14:09] determine exactly what comes out.

[14:11] So there's some constructs there for providing the layout and the design we want to

[14:15] see in a GV turn, so the type of information, the type of supported formats, things

[14:20] like tabbed information, inline scripting, stuff like that.

[14:23] There's a whole bunch of features that we support, like graphics, diagrams inside

[14:28] the return result. And you'll see that.

[14:31] You'll do a turn that's reasonably complex, and every single turn will provide

[14:35] really rich information, unless it's a trivial answer, unless you just ask it

[14:39] what's today's date, it's just going to give you today's date.

[14:41] But if you say to it and talk about a particular architecture, design pattern, or

[14:45] software you're working on, it'll give you detailed information, and it'll lay it

[14:49] out in a really useful way. So, a really big difference and one of our great

[14:53] innovations is the GV turn card. And then those buttons at the bottom, starting

[14:57] with green on the left to brown and off to blue or purple on the right,

[15:03] green is the most recommended next step, and then they're progressively less

[15:09] recommended. They're not don't do, they're just the green button is where the AI is

[15:15] steering you to go, where you should go next, what you should probably do.

[15:19] If it comes up and says, "Audit required," there's a red button and a green button,

[15:24] that means that you've made enough changes where it needs to review its work.

[15:28] We learned early on that most code changes

[15:34] implementation takes a couple of turns.

[15:36] These frontier models from Anthropic and Claude are absolutely incredible, but

[15:42] we realized that very seldom is the code perfect in the first turn.

[15:47] That may change over time, but for now, we've got the platform instructed that

[15:53] after three files are changed in a turn, it'll prompt you for an audit, and you'll

[15:57] see it'll come and say, "Audit required." And you hit the green go button on the

[16:02] audit, and it will check its work. It'll do a self-code review.

[16:06] You can flip over from Claude to Codex, Codex to Claude, or another model, a local

[16:10] LLM, and do your audit there. You don't have to do it with the same model

[16:16] or the same

[16:20] settings for that particular provider.

[16:23] So you could go from Claude Opus to Claude Sonnet if you wanted.

[16:28] I don't recommend that. I'll flip easily, happily from Codex to Claude,

[16:34] Claude to Codex. If I'm using Sol on Codex, their most powerful model,

[16:40] I'll try to use Fable on Claude, and vice versa.

[16:45] Give the audit equivalent thinking and reasoning capability,

[16:50] because otherwise, it could go and regress your code.

[16:56] Anyway, so it allows you to do an audit after three code changes.

[17:00] Highly recommend doing them. You do have a button there to skip the audit.

[17:04] But we've learnt the hard way, get it through the audits. It'll save lots of time.

[17:08] It'll clean up any mistakes it's made.

[17:10] It'll clean up any drift where it's drifted off, update documentation.

[17:14] And then after that, it'll probably prompt you to go and do a commit, Git commit.

[17:18] So that's kind of the next fundamental difference with GreatVibe versus just the

[17:23] vanilla CLIs from

[17:26] Anthropic and OpenAI. Couple more things, you can add your Git credentials, so you

[17:31] can go pull your private Git repos.

[17:34] There's a plus button at the bottom of the screen.

[17:36] Inside that is five or six cards,

[17:42] files, attach,

[17:45] IDE, et cetera. Explore those. In there is a settings one.

[17:49] You can go into settings, then credentials, add a credential for Anthropic, OpenAI.

[17:55] Just go and choose the paste token option, get the token out of your

[18:01] existing client, so whether that's on your Windows desktop or on an existing Linux

[18:05] machine, et cetera, add it in there

[18:09] if needed. But you've got Claude, and you can, on the Mochi node, experiment and

[18:14] play around. You can then go and add your own Linux nodes.

[18:19] You get one free with your account, so you can go and deploy your own Linux node,

[18:23] which you can use as a development machine.

[18:25] The Mochi node is not designed to be your development machine.

[18:28] It hasn't got much disk space, and it's highly underpowered, but it's enough to do

[18:33] a number of turns for you to Ask a question and see how the platform works and so

[18:39] on. But you'll really quickly want to go and deploy a more powerful Linux

[18:45] machine, probably a T4g

[18:51] small, maybe. So you can go into the account admin center to do that.

[18:57] So let's click on the nav bar at the top of the screen, choose your profile

[19:01] picture, click that, and then go to account admin.

[19:03] And from there, you can go into nodes and add a node.

[19:08] It is a complex interface because you can also add organizations, you can add

[19:13] meshes, so collections of nodes working together, et cetera.

[19:17] There's a number of concepts. We've designed this for complex development

[19:22] environments. So i.e., you're working in a team, so multiple developers.

[19:25] Multiple developers looking at the same nodes, looking at the same AI working, or

[19:30] different developers having their own nodes, but wanting to be able to check on

[19:32] each other's turns or just see what's going on.

[19:35] And so we have a concept of meshing, and they're like work groups.

[19:38] They're like little network work groups, so they're totally virtualized.

[19:42] So, you install a gvmesh agent on maybe an on-prem Linux

[19:48] server. You can deploy your own GreatVibe provided nodes.

[19:53] Those are our EC2 instances, virtual machines.

[19:57] And they'll be able to share node information, share turn information.

[20:02] You'll be able to run commands against them on different nodes.

[20:07] And then there's organizations where you can carve up your meshes into different

[20:10] permission groups. Maybe you've got a particular project going on, you can have a

[20:14] mesh just for that, so a collection of virtual servers just focused on that

[20:19] particular project. And then a whole range of them.

[20:22] It's a really powerful architecture.

[20:24] It's like a combination of Git's architecture plus

[20:29] server work group architecture. So, we use it inside Great

[20:34] Vibe. Inside Gravion, I should say.

[20:37] So inside our company, we use it for GreatVibe. We use it for our team.

[20:43] We are a tiny team, but we've got multiple virtual machines that we work on,

[20:47] multiple dev machines. I do all my building on typically two different Linux boxes,

[20:53] both Ubuntu. I've also got a number of macOS machines where the gvmesh agent

[20:58] installed on them, and they all see each other on a mesh, even though some are

[21:02] on-prem, some are here in my home office, and some are in AWS data

[21:08] centers. There's controls there, but they can, in that particular

[21:13] group for me, they can see each other's turn-to-turn history.

[21:17] They can access each other's disks and stuff.

[21:21] So I can have one node run turns on another and vice versa.

[21:24] So I can kind of carve up work. So it's a super powerful and scalable architecture,

[21:29] but you don't need to be worried about that too much right now.

[21:32] Just play around with the Mochi node. When you're ready, go into account admin.

[21:37] So let's click on your picture on the top nav bar, go to the Account admin button,

[21:44] section I should say, and add a node.

[21:48] Add your own new node or go and add a BYO node, i.e., BYO is bring your

[21:54] own. So install the gvmesh agent on your Linux or

[21:59] macOS machine in your office environment, at your home, wherever you're doing your

[22:05] work. And then you'll start to see what you can do from a code

[22:10] development perspective. You can on Mochi go and check out some

[22:16] public Git repos. Maybe you want to do a Git clone of your own public repo or just

[22:22] one that you want to go and explore the code for. You can do that.

[22:26] So just in the prompt box, type in git clone, the name of this.

[22:30] It'll appear in the folder gvsandbox.

[22:34] That's our base sandbox.

[22:38] There is a files explorer interface.

[22:43] You can click on that bottom left-hand side.

[22:45] So click the plus button, and then you'll see it just says Files on the bottom of

[22:49] the tile. Click on that, and then you'll be able to explore the file system on the

[22:55] Linux node that you're on. If you click on the Linux node down on the status bar at

[23:00] the bottom of the screen, that allows you to change to other nodes.

[23:05] So for us, this is how we jump between different machines, and we can run turns on

[23:09] one machine. It's a really powerful platform.

[23:13] Anyway, I'm going to leave this video here.

[23:17] David asked me for just a short two-minute overview, but this has gone on for 25

[23:23] minutes almost. I'm going to do some more videos.

[23:26] We're both going to do some more videos with lots of information on how to use the

[23:29] platform. You'll see the more you explore, there's a ton of features and

[23:33] capabilities, and

[23:37] various ways in which you can configure things.

[23:39] And in fact, you will kind of come to learn that there's almost two ways you can do

[23:43] everything. We've built in different kind of redundant paths for the platform,

[23:50] mainly because people do different things in different ways.

[23:53] So, for example, you could add a credential for one of your AI providers through

[24:00] a prompt, or you could go into the settings and then go into credentials and add

[24:04] credential there. One is through AI, through the prompt, and one is direct on the

[24:09] node itself. So there's no AI involved. But there's also a third way.

[24:13] You can go into

[24:18] the settings, and you'll see a button there called Secrets, and that is a secure

[24:22] vault system where whatever you enter in the box inside the input text area,

[24:29] it is

[24:31] only visible

[24:35] on the node. So we have an encrypted trust chain between your browser

[24:40] right through to the node when you go into the secure vault.

[24:44] You can put any secret in there, it'll get put on your node, and then you can do a

[24:48] prompt telling AI to do something with it.

[24:51] And what that does is it allows you to provide your secure credentials

[24:57] for your important services, GitHub, et cetera.

[24:59] Maybe you want to use your account, get to a private repo.

[25:03] You can do that by using secure vault to transfer that credential down to the node.

[25:07] It'll put it into an encrypted place on the node.

[25:12] Maybe it's in our encryption store or encrypted store for creds

[25:18] inside the node and then use it for any kind of Git-based turns or tool calls

[25:23] inside turns, et cetera. So that's the secure vault.

[25:26] That's a really new functionality. We're really proud of it.

[25:30] It allows you to get your most

[25:36] sensitive information down to a node where you need it to be without any of the

[25:40] models or the frontier

[25:43] providers or staff at GreatVibe being able to see that credential or decrypt it.

[25:48] Anyway, go in there and have a look at it.

[25:49] It's got a complete trust chain that's visible.

[25:52] You can audit it, and check to make sure it's all live, and it's completely trusted

[25:57] end to end. Okay, that's it for now. Enjoy the platform.

[26:01] We'll do some more videos soon. And thanks for trying our platform
