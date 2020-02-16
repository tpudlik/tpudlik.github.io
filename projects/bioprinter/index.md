---
layout: page
excerpt: "Cell jet printer."
title: Bioprinter
tags: [Ted Pudlik, Tadeusz Pudlik, bioprinter]
share: false
image:
  feature: bioprinter-header-2.JPG
---

At [Science Hack Day Boston][] 2015 I joined a team led by  [Dan Burkhardt][]
working on a "bioprinter": a 2D printer based on the [InkShield][], designed
to print cells directly on Petri dishes.  The basic idea is to use an Arduino
to control both an ink head and a pair of stepper motors, one for each degree
of freedom.  In our implementation, the Arduino accepts  sequences of
[G-codes][],  sent one by one over the serial port.  Together with
[Pascal Timshel][], I wrote the Python software that converts PNG images provided by the user into the G-codes and sends them to the Arduino.

By the end of the hackathon, we had a proof-of-concept design and were able to
print arbitrary patterns with ink. Since then, Dan (who at the time worked in
a biology lab at UMass) has used the device to print actual cells.

<figure class="half">
    <a href="{{ site.url }}/images/bioprinter_in_action.JPG"><img src="{{ site.url }}/images/bioprinter_in_action.JPG"/></a>
    <a href="{{ site.url}}/images/petri_dish.JPG"><img src="{{ site.url }}/images/petri_dish.JPG"></a>
    <figcaption>
        Bioprinter in action (but with regular ink) and actual cells printed
        by Dan later.
    </figcaption>
</figure>

To learn more about the bioprinter, check out the
[host](https://github.com/tpudlik/bioprinter_host) and
[Arduino](https://github.com/tpudlik/bioprinter_arduino) software on GitHub
and visit [Dan's blog][]. The original inspiration for this project was
[this instructable](https://www.instructables.com/id/DIY-BioPrinter/)
by [BioCurious](https://biocurious.org/).


[Science Hack Day Boston]: https://sciencehackdayboston.wordpress.com/
[Dan Burkhardt]: https://scienceroastery.wordpress.com/
[Dan's blog]: https://scienceroastery.wordpress.com/2015/02/05/bioprinter-part-3/
[InkShield]: https://nicholasclewis.com/projects/inkshield/
[G-codes]: https://en.wikipedia.org/wiki/G-code
[Pascal Timshel]: https://github.com/pascaltimshel
