---
layout: page
excerpt: "Let birds leave you postcards."
title: Paparazzi bird feeder
tags: [Jekyll, theme, responsive, template]
share: false
image:
  feature: header-tufted_titmouse.jpg
---

I keep a bird feeder outside a window at home, but I can never be sure who
visits it: when the birds are awake, I'm at work (or asleep).  The paparazzi
bird feeder solves this problem by taking pictures of my avian visitors and
posting them to [Flickr][] and [Twitter][].

    
I started working on this idea at [Triangle Startup Weekend][]: Maker Edition
in April 2014 with [Aaron Mead][] and [Andrew Roberson][]. In the beginning,
we had only some rough sketches:

<figure>
    <a href="{{ site.url }}/images/Dry_Erase_Board.jpg"><img src="{{ site.url }}/images/Dry_Erase_Board.jpg"></a>
    <figcaption>Our dry-erase board.</figcaption>
</figure>

We quickly built a working prototype that detected the birds using a passive
IR sensor and a sonic ranger:

<figure>
    <a href="{{ site.url }}/images/prototype.JPG"><img src="{{ site.url }}/images/prototype.JPG"/></a>
    <figcaption>The cardboard prototype.</figcaption>
</figure>

It took pictures like this one, showing a family of house finches:

<figure>
    <a href="{{ site.url }}/images/2014-07-06-11-42-36.jpeg"><img src="{{ site.url }}/images/2014-07-06-11-42-36.jpeg"/></a>
    <figcaption>Bird spotted!</figcaption>
</figure>

You'll notice that this early prototype was made of cardboard, so it could
only be deployed when the weather was good.  The detection strategy was not
very reliable, either: almost one picture in four were false positives.

The current prototype addresses these shortcomings.  The passive IR sensor and
sonic ranger were replaced with a modulated-IR tripwire, and the electronics
was moved into a weatherproof box.

<figure>
    <a href="{{ site.url }}/images/plywood-prototype.JPG"><img src="{{ site.url }}/images/plywood-prototype.JPG"/></a>
    <figcaption>The plywood prototype.</figcaption>
</figure>

For more images and instructions for building your own, check out
[the project's website](http://www.birdfeeder.camera).  You can also follow
the prototype on [Flickr][].

<figure class="third">
    <a href="/images/sparrows-big.jpg"><img src="/images/sparrows.jpg"></a>
    <a href="/images/nuthatches-big.jpg"><img src="/images/nuthatches.jpg"></a>
    <a href="/images/bluejay-big.jpg"><img src="/images/bluejay.jpg"></a>
    <figcaption>
        A few of my favorite pictures: quarreling sparrows, a pair of
        nuthatches, and a bluejay hiding from the rain.
    </figcaption>
</figure>


[Aaron Mead]: http://aaronmead.com/
[Andrew Roberson]: https://www.linkedin.com/in/andrewroberson
[Flickr]: https://www.flickr.com/photos/131794461@N04
[Twitter]: https://twitter.com/paparazzifeeder
[Triangle Startup Weekend]: http://trianglemaker.startupweekend.org/
