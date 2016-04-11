---
layout: page
excerpt: "Raspberry Pi hydroponics system."
title: HydroPi
tags: [Raspberry Pi, hydroponics]
image:
  feature: header-hydroponics-2.jpg
---

Growing herbs sounds easy in principle: you buy a basil plant at the grocery
store, place it in a sunny spot and water it regularly.  In practice, I have
never kept a living plant in the soil for longer than a month (excepting
cacti, which make poor salad material).  Sooner or later, as the plant grew,
I always failed to strike the right balance between over- and
under-watering the soil.

You can't grow basil and other herbs without watering, but it turns out you
*can* grow them without the soil.  Ditch the dirt, suspend the root system in
an oxidized nutrient solution, and you have a hydroponics system.  If you
toss in artificial lighting, the environment of the plant can be fully
controlled, producing reliable yields even if you don't know the first thing
about gardening.

In early 2016, after experimenting with small out-of-the-box systems, my wife
and I decided to build a custom hydroponics system.

<figure>
    <a href="{{ site.url }}/images/assembled_system.jpg"><img src="{{ site.url }}/images/assembled_system.jpg"></a>
    <figcaption>Our hydroponics system shortly after assembly.</figcaption>
</figure>

The biggest obstacle was constructing a frame that would hold the
plants, the nutrient solution, and the lights.  Many DIY systems use PVC
pipes for this ([two][ex1] [examples][ex2]), but cutting and assembling PVC
seemed like a lot of hassle.  Eventually, we decided to use an Ikea
[TROFAST][] cabinet to hold all components together.  This was an excellent
choice: the assembly was easy and the finished frame is very stable.  As a
bonus, both the plant drawers and the light fixtures can be pulled out, and
their height can be adjusted.

Other than the TROFAST, our approach was traditional: LED strips for
illumination and an aquarium pump for aeration.  Since the lights should only
be on for a certain number of hours per day, and the pump run briefly every
hour, we use a Raspberry Pi to turn them on and off.  The Pi also serves a
minimal web application that allows "quiet mode" to be enabled for a given
time.  During "quiet mode", the lights and pump will stay off.

If you are considering building your own hydroponics system, you can find our
list of materials, assembly instructions, and software [on GitHub][gh].

<figure>
    <a href="{{ site.url }}/images/closeup.jpg"><img src="{{ site.url }}/images/closeup.jpg"></a>
    <figcaption>Basil, parsley, cilantro and dill after about a month.
    </figcaption>
</figure>

[ex1]: http://www.instructables.com/id/Vertical-Hydroponic-Farm/
[ex2]: http://www.instructables.com/id/My-Indoor-DWC-Hydroponics-System/
[gh]: https://github.com/tpudlik/hydroponics
[TROFAST]: http://www.ikea.com/us/en/catalog/categories/series/19027/