---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 40

title: Experience
subtitle:

# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
experience:


  - title: Graduate Research Assistant
    company: Rensselaer Polytechnic Institute
    company_url: 'https://www.rpi.edu/'
    location: NY
    date_start: '2017-08-20'
    date_end: ''
    description: |4-
        
        * Developed a framework for cross-domain few-shot learning that uses unlabeled images from novel dataset during meta-training.  
        * Proposed a weakly supervised temporal action localization method using metric learning that only requires video-level action instances as supervision during training. Also developed a deep learning model with _hybrid attention mechanism (HAMNet)_ for solving the issues of action completeness and background modeling in temporal action localization with weak supervision, outperforming SOTA methods by atleast 2.8%.
        * Developed a system that automatically tracks passengers and items, and detects unusual activities (baggage theft, left-behind items, etc.) at an airport security checkpoint (demo [video](https://drive.google.com/file/d/1KNUabcVEKMsFvQQ1u_NB5ZI6J9kRHuEe/view?usp=sharing)).


  - title: Research Intern
    company: IBM Research
    company_url: 'https://www.research.ibm.com/labs/watson/'
    location: NY
    date_start: '2020-06-11'
    date_end: '2020-08-27'
    description: I researched on unsupervised and supervised contrastive representation learning for transfer learning. Our study suggests that networks trained with contrastive loss is more transferable to a different domain than the networks trained with supervised cross-entropy loss. Proposed and analyzed joint objective of self-supervised contrastive loss with cross-entropy or supervised contrastive loss that leads to better transferability of these models over their standard-trained counterparts.

        
  - title: Research Intern
    company: Kitware Inc.
    company_url: 'https://www.kitware.com/'
    location: NY
    date_start: '2019-05-18'
    date_end: '2019-08-18'
    description: I developed a deep adversarial model titled 'Dual-order Attentive Generative Adversarial Network (DOA-GAN)' for image and video copy-move forgery detection and localization.
---
