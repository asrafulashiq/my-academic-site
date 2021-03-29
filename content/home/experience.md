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
  - title: Research Intern
    company: IBM Research
    company_url: 'https://www.research.ibm.com/labs/watson/'
    location: NY
    date_start: 'July 2020'
    date_end: 'Aug 2020'
    description: |2-
        Responsibilities include:
        
        * Analysed unsupervised and supervised contrastive representation learning for transfer learning in downstream linear evaluation, full-network transfer, few-shot recognition, and object detection tasks, suggesting that networks trained with contrastive learning is more transferable to a different domain than the networks trained with supervised cross-entropy loss.  
        * Proposed joint objective of self-supervised contrastive loss with cross-entropy or supervised contrastive loss, that leverages both inter-class and intra-class separability leading to better transferability of these models over their standard-trained counterparts (*5.44*% improvement over cross-entropy models in linear evaluation protocol).

        
  - title: Research Intern
    company: Kitware Inc.
    company_url: 'https://www.kitware.com/'
    location: NY
    date_start: 'May 2019'
    date_end: 'Jul 2019'
    description: Developed a deep adversarial model titled 'Dual-order Attentive Generative Adversarial Network (_DOA-GAN_)' for image and video copy-move forgery detection and localization, where the first-order attention is designed to capture copy-move location information, and the second-order attention exploits more discriminative features for the patch co-occurrence.
---
