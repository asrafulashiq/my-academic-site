---
title: 'Home'
date: 2023-10-24
type: landing

design:
  # Default section spacing
  spacing: '4rem'

# Page sections
sections:
  - block: biography
    id: about
    content:
      username: admin
      # Show a call-to-action button under your biography
      button:
        text: Download CV
        url: https://drive.google.com/open?id=1zdJIzxfl8LTjYx-GNwI48st9i9fEnhvx&usp=drive_fs
    design:
      biography:
        style: 'text-align: justify; font-size: 0.9em;'
      avatar:
        size: large
        shape: rounded

  - block: experience
    id: experience
    content:
      username: admin
    design:
      date_format: 'January 2006'
      is_education_first: false

  - block: skills
    id: skills
    content:
      title: Skills
      username: admin

  - block: collection
    id: publications
    content:
      title: Publications
      filters:
        folders:
          - publication
    design:
      view: citation

  - block: awards
    id: awards
    content:
      title: Awards
      username: admin
---
