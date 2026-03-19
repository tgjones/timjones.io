---
title:   "Shutting down Shader Playground"
date:    2026-03-18 23:00:00 UTC
excerpt: "Announcing shutdown of the Shader Playground website"
tags:    shaders shader-playground
---

After nearly 8 years, I'm shutting down [Shader Playground](http://shader-playground.timjones.io). To minimize disruption I'll wait a few weeks after this announcement before doing so. I plan to do the actual shutdown at the end of April 2026.

The [source code on GitHub](https://github.com/tgjones/shader-playground) will remain available.

Links that have been created via "Share Permalink" will cease to function, _but_ the underlying shaders are not lost:
ß
* If the permalink was e.g. <https://shader-playground.timjones.io/8a375ffa08307f6fd746ce6a76b79692>
* Then replace the first part with <https://gist.github.com/shader-playground/>, e.g. <https://gist.github.com/shader-playground/8a375ffa08307f6fd746ce6a76b79692>
* ... and you'll find your shader code

For an alternative online shader compiler, I highly recommend [Godbolt / Compiler Explorer](https://godbolt.org).

## A brief history

I launched Shader Playground in [May 2018](/blog/archive/2018/05/19/introducing-shader-playground) as a kind of [Compiler Explorer](https://godbolt.org/) for shading languages. The idea was simple: paste in some HLSL or GLSL, pick a compiler, and see what comes out the other side. You could chain compilers together — compile HLSL to SPIR-V with DXC, then feed that into SPIRV-Cross to get Metal. You could share a permalink. It scratched an itch I had, and apparently quite a few other people found it useful too.

## Why shut it down?

Two reasons.

First, [Compiler Explorer](https://godbolt.org/) now supports most of the most-used compilers on Shader Playground — DXC, RGA, SPIRV-Cross, glslang, Slang. It even has one that Shader Playground doesn't: the new Clang-based HLSL compiler. In my opinion, this is an ideal outcome. Godbolt has an incredible feature set, a huge community, and deep institutional support. It just makes sense for it to be the home for shader compiler exploration too. I think Shader Playground played a useful role in demonstrating the appetite for this kind of tool, but Godbolt is the better home for it. Perhaps unsurprisingly, traffic to Shader Playground has been steadily declining as Godbolt's shader support has grown.

Second, my own time and motivation to keep Shader Playground updated have both decreased. Shader Playground was (I like to think) a genuinely useful resource for a while, but it's an idea whose time has come and gone now that Godbolt covers the same ground better.

## One gap: Metal

The one area where Shader Playground still has something Godbolt doesn't is Metal support. As part of this shutdown, I'm going to try to fill that gap by contributing Metal support to Godbolt itself, via the [Metal developer tools](https://developer.apple.com/metal/tools/) that Apple ships for Windows. Watch this space.

## Some numbers

Just for fun, here are some numbers.

Since I started collecting analytics in September 2017 (back when it was called [Try HLSL](/blog/archive/2017/02/11/try-hlsl-online)):

* 47,592 unique users...
* ... have done 720,102 shader compilations
* ... across 8 languages (GLSL, HLSL, Metal, OpenCL, Rust, Slang, SPIR-V, WGSL)
* ... and 23 compilers (ANGLE, Clspv, dxc, fxc, GLSL optimizer, glslang, hlsl2glsl, HLSLcc, HLSLParser, Intel Shader Analyzer, Mali offline compiler, Metal developer tools, Naga, PowerVR compiler, RGA, Rust GPU, Slang, SPIRV-Cross, SPIRV-Cross (ISPC), spirv-as, spirv-opt, Tint, XShaderCompiler)

I think this little website has done alright.

## Thanks

My thanks to everyone who used the site, filed issues, or submitted PRs over the years. You made it what it was. It was a fun project to build and I'm glad it was useful while it lasted.

And most especially, my heartfelt thanks to the sponsors on Patreon and GitHub Sponsors who helped me pay the hosting costs over the 8 years this site has been running (this list includes all sponsors, present and past): Aras Pranckevičius, Laura Reznikov, Inês Almeida, Tom Forsyth, Joel de Vahl, Sean Cooper, Ryszard Sommefeldt, David Neto, Aishization, Neil Henning, Dimitri Diakopoulos, Johan Andersson, Ikrima, Nathan Reed, Jérémie St-Amand.