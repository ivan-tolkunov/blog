---
title: "A Remote Dev Environment Was All I Needed"
date: "2026-08-27"
summary: "I turned my underpowered Linux laptop into a thin client for a remote agentic dev setup instead of replacing it."
tags:
  - linux 
  - workflow 
  - personal
---

I've been using Linux as my main OS for the last year. My laptop is a base [Framework 13 Ultra Series 1 DIY Edition](https://frame.work/ca/en/products/laptop13-diy-amd-ai300/configuration/new) with 16 GB of memory.

For a long time, that was enough. I used it for coding, everyday work, browsing, music, and normal development. I was happy because I finally had something that felt like an Apple alternative, but with a system I could shape exactly how I wanted.

Then my coding workflow changed.

I moved from mostly writing code in an IDE to working with coding agents. Suddenly I wanted [Zed](https://zed.dev/) with multiple LSPs, OpenCode/Pi/Claude Code running at the same time, a local server for testing changes, a browser, music, and all the usual background stuff.

16 GB stopped being enough very quickly.

I kept increasing swap, but that was only a patch. Eventually I would hit a point where the whole system slowed down or almost froze. It became painful enough that I seriously considered going back to a Mac.

macOS is very well optimized, and a MacBook would probably solve most of these problems immediately. But I didn't really want to leave Linux.

I put a lot of effort into my setup. It works exactly how I want: almost no animations, fast, stable, and completely mine. Linux also became a bit addictive. Once you get used to being able to change almost anything, it's hard to give that up. I really started living by Framework's "Fix It Yourself" philosophy.

Then I found a post about [Herdr](https://herdr.dev/), an alternative to [Zellij](https://zellij.dev/).

I had already been using Zellij, but probably not anywhere near its full potential. Most of the time I used it to move between projects and tabs. I rarely used panes heavily.

Herdr immediately made more sense for my workflow. It feels more focused on agents and agent-based development, while still giving me the parts of Zellij I actually used. The UI also fits me better, so switching was easy.

Cool. New shiny tool.

But I still had the same memory problem.

While reading the Herdr documentation, I noticed that it supports remote sessions.

That gave me an idea.

I have another machine with a 3080 Ti sitting in my server room. I originally built it mostly for fun: testing [ComfyUI](https://comfy.org/) workflows, running small LLMs, and occasionally streaming games through [Moonlight](https://moonlight-stream.org/).

Most of the time it was basically abandoned.

So I decided to turn it into my dev machine.

I configured SSH, installed my Git SSH keys, added [Tailscale](https://tailscale.com/) so I can reach it from anywhere, installed Herdr, [Pi](https://pi.dev/), and recreated my development environment there.

About two hours later, I had my normal dev setup running remotely, including the shortcuts and workflow I was already used to.

My server is called `kurama`, because of Naruto, so now I can just run:

`herdr remote kurama`

And that's basically it.

Now I can interact with everything remotely without any real issues. Zed also has a nice feature that lets me view changes directly in the project folder on a server, so the experience is very close to how I worked before switching to an agent-based workflow.

I also don't need to worry about keeping my laptop awake with `Keep Awake`. I can just close the lid and leave the agents running on Kurama.

The next thing I want to find or build is a small dashboard I can check from my phone. That way I could go for a walk, see how the agents are progressing, and jump in when I need to give feedback or steer them in a different direction.

I can sit on my Framework and prompt Pi while the agents, LSPs, servers, and other development tools are running on Kurama. The interaction feels almost local, but my laptop RAM usage stays low enough that I can keep using the browser, music, and everything else without the machine struggling.

Instead of replacing my Framework with a more powerful laptop, I accidentally turned it into a thin client for a much more powerful Linux development machine.

And I get to keep the Linux setup I spent the last year building.

PS: Maybe this is all on me and I just have _skill issues_. I could probably fix some of this with better optimizations, but for now I'm going to call it a _memory issue_ :)
