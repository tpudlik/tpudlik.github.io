---
layout: page
title: Fountain camera
share: false
image:
  feature: header-fountain.jpg
---

I first dabbled in bird photography more than a decade ago, with the
[Paparazzi birdfeeder](../birdfeeder/index.md). This is my most recent effort,
from 2026, lighter on the hardware but heavier on the software.

My garden has a fountain that's often visited by birds that drink or bathe
there. I was curious what species visit me and when, so I set up a Raspberry Pi
with a
[High Quality Camera module](https://www.raspberrypi.com/products/raspberry-pi-high-quality-camera/)
and a
[16 mm telephoto lens](https://www.pishop.us/product/16mm-telephoto-lens-for-raspberry-pi-hq-camera-cs/).
The Pi just takes pictures, one every 5 minutes, and uploads them to a GCS
bucket. From there, a Cloud Run job runs a bird detector (currently a D-FINE XL
trained on Objects365, `ustc-community/dfine-xlarge-obj365`) and a classifier
(EVA-02 Large fine-tuned on iNaturalist 2021,
`timm/eva02_large_patch14_clip_336.merged2b_ft_inat21`). I save the crops of any
detected birds, and display them on
[https://fountain.tpudlik.com](https://fountain.tpudlik.com).

Some reflections on this project:

- Thanks to a lot of help from Claude, I put it together in about a month of
  occasional evening hacking, which is a really astonishing pace. It clocks in
  at over 17,000 lines of Go and Python, including fun little touches like a
  custom labeling tool for the photos, and some surprisingly gnarly data
  wrangling, like reconciling iNaturalist species names (used by the classifier)
  with those from
  [eBird species lists](https://ebird.org/region/US-CA-075/bird-list) (used to
  restrict the IDs to birds that can actually be seen where I live). Before
  2026, a project like this would have easily taken a month of full-time work,
  even if I was an expert in all the relevant technologies, which I am not. I
  would not even have attempted a project of such scope---which is a big reason
  why I've done so few side projects since finishing graduate school!

- When I first started working on the paparazzi birdfeeder, in North Carolina in
  2013, just classifying the birds would have been a research project in
  Computer Science. Now I basically[^crop] just used some off-the-shelf models.
  It's not perfect, but mostly it works!

[^crop]:
    One exception is that cropping the photo to just the region containing the
    rim of the fountain (even smaller than what's in the header image) helps a
    lot with recall. I'm tempted to add more cropping or masking to remove the
    false positives from the water jet in the fountain's center.

- If I was getting all the hardware from scratch, I would have probably splurged
  on a Raspberry Pi 5, and attempted to run at least detection locally. But I
  had an original (2012!) Model B at hand, and just used that. Unfortunately,
  the outdated CPU would have required compiling a lot of software from source,
  and it looked like maintaining even a 5 minute photo processing cadence could
  be a challenge, so I put all the processing in the cloud.
