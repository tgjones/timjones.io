---
title:   "Xbox One XDK shader intrinsics now available in HLSL Tools for Visual Studio"
date:    2017-03-21 22:02:00 UTC
excerpt: "Xbox One XDK shader intrinsics are now available in HLSL Tools for Visual Studio"
tags:    HLSL HLSL-Tools
---

I'm very happy to announce that the latest version of [HLSL Tools for Visual Studio](https://marketplace.visualstudio.com/items?itemName=TimGJones.HLSLToolsforVisualStudio) (v1.1.197 at the time of writing) includes full IntelliSense support for Xbox One XDK shader intrinsic functions.

{% responsive_image path: assets/posts/xdk-intrinsics-1.png %}

If you don't write games for the Xbox One, then feel free to stop reading now; but if you do, then I think you'll find this really useful. You get statement completion, signature help, and quick info for these shader intrinsics (all but one of which is prefixed by `__XB_`, so these functions won't clutter things up for non-XDK HLSL developers).

{% responsive_image path: assets/posts/xdk-intrinsics-2.png %}

If you write shaders for the Xbox One, then give [HLSL Tools for Visual Studio](https://marketplace.visualstudio.com/items?itemName=TimGJones.HLSLToolsforVisualStudio) a try! As always, let me know if you find any bugs. In terms of feature requests, please [read this note before requesting additional intrinsics or other functionality from the XDK](https://github.com/tgjones/HlslTools/blob/master/CONTRIBUTING.md#note-about-the-xbox-one-xdk) (basically, if you've signed an NDA for this stuff, then you're still under that NDA).

I'd like to give a big shout-out to [Adam Miles](https://twitter.com/adamjmiles) for making this feature possible; he did almost all the hard work, including documenting the intrinsics themselves.

Happy coding!