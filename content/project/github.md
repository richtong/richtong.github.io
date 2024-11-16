---
title: GitHub Bin and Lib Utilities
# remove date to use weight
# date: "2023-10-24T13:50:46+02:00"
weight: 1
banner: "img/solution/github.com.png"
banner-gen: >

  {
      "prompt": "software utilities useful happy\n\n\n\n\n",
      "is_adv_mode": false,
      "selected_sd_model": "FLUX.1-dev",
      "selected_aspect_ratio": "Landscape",
      "num_imgs": 1,
      "selected_sd_style": "enhance",
      "applet_name": "txt2img",
      "available_text_emb_words": {},
      "img_width": 896,
      "img_height": 704,
      "num_steps": 25,
      "pipeline": "flux",
      "flux_model_type": "dev",
      "image_no": 0,
      "seed": 688610
  }

description: >
  Rich's fine utilities
---

I never thought this would last that long, but in 2014, it was really hard to
get a stable configuration across machines, so I started writing `install.sh` to
make this easy. That's grown into a general installer that is targeted at the
MacOS right now, but has worked with Ubuntu and WSL on Windows. There are two
places for documentation. The README of course and there are two mkdocs sites:

- [Bin](/bin). These are mainly shell scripts that install things.
- [Lib](/lib). These are supporting library

<!--more-->
