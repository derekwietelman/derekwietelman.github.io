---
# Homepage. Each item under `sections` is one block on the page, shown in order.
title: ''
summary: ''
date: 2026-10-20
type: landing

sections:
  - block: resume-biography-3
    id: about
    content:
      # Profile details (name, role, links) live in `data/authors/me.yaml`.
      username: me
      text: |-
        Welcome to my personal research website. I am a [Postdoctoral Associate](https://ibs.colorado.edu/people/derek-wietelman/) at the [University of Colorado Boulder](https://www.colorado.edu), housed in the [Institute of Behavioral Science](https://ibs.colorado.edu). In 2026, I received my Ph.D. from the [Department of Agricultural and Resource Economics](https://arec.umd.edu) at the [University of Maryland](https://umd.edu).\*

        I am an ***applied microeconomist*** who specializes in ***environmental and resource economics***. Much of my current research studies the pricing and allocation of energy and water resources during periods of scarcity, such as [peak electricity demand hours](/publications/ecobee/) or [severe droughts](/publications/bbr/). Currently, I am investigating how drought-induced conservation mandates interact with existing, inefficient water prices.

        In addition to my work on resource ***quantities***, I also maintain an active research agenda in the economics of environmental ***quality***, particularly water quality. In this work, I characterize [long-run trends in surface water quality](/publications/texas/) and examine how policy design impacts nonpoint source pollution from both the [agricultural](/publications/trading/) and residential sectors. Currently, I am working to identify how variation in lead remediation efforts (e.g., service line replacements by water utilities) affects health and behavioral outcomes.

        \* All conclusions in the writings presented here are my own and do not necessarily represent the views of any of my employers, past or present.
        {.bio-note}
      button:
        text: Download CV
        url: /files/cv.pdf
      headings:
        about: Biography
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle

  - block: collection
    id: working-papers
    content:
      title: Working Papers
      filters:
        folders:
          - publications
        publication_type: article
      count: 0
    design:
      view: citation

  - block: collection
    id: publications
    content:
      title: Publications
      filters:
        folders:
          - publications
        publication_type: article-journal
      count: 0
    design:
      view: citation

  - block: contact-info
    id: contact
    content:
      title: Contact
      visit_title: Mailing Address
      connect_title: Connect
      address:
        lines:
          - Institute of Behavioral Science
          - University of Colorado Boulder
          - 483 UCB
          - Boulder, CO 80309-0483
      email: derek.wietelman@colorado.edu
      social:
        - icon: hero/building-library
          url: https://ibs.colorado.edu/people/derek-wietelman/
          label: CU Boulder profile
        - icon: brands/github
          url: https://github.com/derekwietelman
          label: GitHub
        - icon: academicons/google-scholar
          url: https://scholar.google.com/citations?user=4fMH-1cAAAAJ
          label: Google Scholar
        - icon: brands/linkedin
          url: https://www.linkedin.com/in/derek-wietelman-2b351b146
          label: LinkedIn
        - icon: academicons/researchgate
          url: https://www.researchgate.net/profile/Derek-Wietelman
          label: ResearchGate
      show_form: false
---
