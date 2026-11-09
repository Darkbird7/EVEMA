# Third-party notices

EVEMA incorporates material from the projects below. Their licenses require that
these notices be retained in distributions. EVEMA's own license (`LICENSE`) does not
limit the rights these licenses give you.

## BlueMarshal

EVEMA's reader and writer for EVE's settings files, the BlueMarshal library, is
licensed separately from EVEMA under the MIT License:

```
MIT License

Copyright (c) 2026 Darkbird

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Fenris Creations (formerly CCP Games) — Carbon Engine, `blue` module

The blue.Marshal type codes in `BlueMarshal/MarshalType.cs`, and the stream
layout `BlueMarshal/MarshalReader.cs` implements, are taken from the `PYTYPES`
enumeration and marshalling logic in `src/Marshal.h` and `src/Marshal.cpp` of
Fenris Creations' MIT-licensed [`carbonengine/blue`](https://github.com/carbonengine/blue)
repository (`release/2.x`). This notice is duplicated in `BlueMarshal/NOTICE`
so it travels with the library if it's ever extracted into its own repository.

```
Copyright (c) 2026 CCP Games

MIT License
```

EVE Online and all related logos and images are trademarks of Fenris Creations (formerly CCP hf.). EVEMA is
not affiliated with, endorsed by, or sponsored by Fenris Creations (formerly CCP hf.).

## TrueBrain — blue-marshal-rs

[`TrueBrain/blue-marshal-rs`](https://github.com/TrueBrain/blue-marshal-rs) was
the reference that identified where Fenris Creations' published marshalling source lives.
No code from it is included in EVEMA; it is credited because the pointer is what
made a correct implementation possible. It is also used as a cross-check when
reading Fenris Creations' source, for example on when the loader registers shared
objects.

```
Copyright (c) 2026 TrueBrain

MIT License
```

## EVE Wrench

[`eve-wrench/eve-wrench-app`](https://github.com/eve-wrench/eve-wrench-app) (MIT)
was studied as prior art for feature scope and for its attribution trail. Facts
EVEMA took from it, each checked against real settings files or in game: which
settings keys make up each copy group, the probe formation axis convention (+x
West, +y Up, +z North), the layouts of the Drifter and directional-stack probe
presets, its note that the client re-centres a formation on the probes'
average position, and where drone groups are stored (`droneBlah2`) and the idea of
naming them from a pattern. No code or data from it is included in EVEMA: the drone
catalog and its stats come from the Static Data Export below.

## Fenris Creations (formerly CCP Games) — Static Data Export

The drone families and their stats in `EVEMA.Core/Settings/Drones/drone-catalog.json`
are derived from Fenris Creations' [Static Data Export](https://developers.eveonline.com/docs/services/static-data/)
by `tools/DroneCatalog`, under the developer licence EVEMA is registered with. The
catalog names the SDE build it came from. The SDE itself is not distributed with EVEMA.

## Avalonia

EVEMA's user interface is built on [Avalonia](https://github.com/AvaloniaUI/Avalonia)
(`Avalonia`, `Avalonia.Desktop`, `Avalonia.Themes.Fluent`, `Avalonia.Controls.DataGrid`,
`Avalonia.Skia` and their platform packages), distributed under the MIT License.

```
Copyright 2013-2026 (c) The AvaloniaUI Project

MIT License
```

The `Fluent` theme and the DataGrid control's default templates are part of that project.

## SkiaSharp, Skia and HarfBuzzSharp

Avalonia renders through [SkiaSharp](https://github.com/mono/SkiaSharp) (MIT License,
Copyright (c) Microsoft Corporation / Xamarin Inc.), which bundles Google's
[Skia](https://skia.org/) graphics library (BSD 3-Clause License, Copyright (c) 2011 Google Inc.),
and text is shaped by [HarfBuzzSharp](https://github.com/mono/SkiaSharp) (MIT License) over
[HarfBuzz](https://github.com/harfbuzz/harfbuzz) (Old MIT License, Copyright (c) the HarfBuzz
authors). Their native libraries ship inside the self-contained release builds.

## Inter (typeface)

The bundled UI typeface comes from the `Avalonia.Fonts.Inter` package and is
[Inter](https://rsms.me/inter/), licensed under the SIL Open Font License, Version 1.1.

```
Copyright (c) 2016 The Inter Project Authors (https://github.com/rsms/inter)

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
https://openfontlicense.org

-----------------------------------------------------------
SIL OPEN FONT LICENSE Version 1.1 - 26 February 2007
-----------------------------------------------------------

PREAMBLE
The goals of the Open Font License (OFL) are to stimulate worldwide
development of collaborative font projects, to support the font creation
efforts of academic and linguistic communities, and to provide a free and
open framework in which fonts may be shared and improved in partnership
with others.

The OFL allows the licensed fonts to be used, studied, modified and
redistributed freely as long as they are not sold by themselves. The
fonts, including any derivative works, can be bundled, embedded,
redistributed and/or sold with any software provided that any reserved
names are not used by derivative works. The fonts and derivatives,
however, cannot be released under any other type of license. The
requirement for fonts to remain under this license does not apply
to any document created using the fonts or their derivatives.

DEFINITIONS
"Font Software" refers to the set of files released by the Copyright
Holder(s) under this license and clearly marked as such. This may
include source files, build scripts and documentation.

"Reserved Font Name" refers to any names specified as such after the
copyright statement(s).

"Original Version" refers to the collection of Font Software components as
distributed by the Copyright Holder(s).

"Modified Version" refers to any derivative made by adding to, deleting,
or substituting -- in part or in whole -- any of the components of the
Original Version, by changing formats or by porting the Font Software to a
new environment.

"Author" refers to any designer, engineer, programmer, technical
writer or other person who contributed to the Font Software.

PERMISSION & CONDITIONS
Permission is hereby granted, free of charge, to any person obtaining
a copy of the Font Software, to use, study, copy, merge, embed, modify,
redistribute, and sell modified and unmodified copies of the Font
Software, subject to the following conditions:

1) Neither the Font Software nor any of its individual components,
in Original or Modified Versions, may be sold by itself.

2) Original or Modified Versions of the Font Software may be bundled,
redistributed and/or sold with any software, provided that each copy
contains the above copyright notice and this license. These can be
included either as stand-alone text files, human-readable headers or
in the appropriate machine-readable metadata fields within text or
binary files as long as those fields can be easily viewed by the user.

3) No Modified Version of the Font Software may use the Reserved Font
Name(s) unless explicit written permission is granted by the corresponding
Copyright Holder. This restriction only applies to the primary font name as
presented to the users.

4) The name(s) of the Copyright Holder(s) or the Author(s) of the Font
Software shall not be used to promote, endorse or advertise any
Modified Version, except to acknowledge the contribution(s) of the
Copyright Holder(s) and the Author(s) or with their explicit written
permission.

5) The Font Software, modified or unmodified, in part or in whole,
must be distributed entirely under this license, and must not be
distributed under any other license. The requirement for fonts to
remain under this license does not apply to any document created
using the Font Software.

TERMINATION
This license becomes null and void if any of the above conditions are
not met.

DISCLAIMER
THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL THE
COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL, OR CONSEQUENTIAL
DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF THE USE OR INABILITY TO USE THE FONT SOFTWARE OR FROM
OTHER DEALINGS IN THE FONT SOFTWARE.
```

## Microsoft .NET libraries and CommunityToolkit.Mvvm

The .NET runtime bundled in the self-contained release builds, the
`Microsoft.Extensions.*` packages and [CommunityToolkit.Mvvm](https://github.com/CommunityToolkit/dotnet)
are distributed under the MIT License (Copyright (c) .NET Foundation and Contributors).
