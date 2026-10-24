---
# Contact page: contact cards with a photo beside them (block defined in
# layouts/_partials/hbx/blocks/contact-photo/). Photo files go in `assets/media/contact/`.
title: Contact
type: landing
# Keep it out of the theme's page list in the phone menu on paper pages.
sidebar:
  hidden: true

sections:
  - block: contact-photo
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
      image: contact/boulder-creek.jpg
      image_alt: Boulder Creek flowing between rocky, tree-lined banks
      caption: A view from a lunchtime walk along Boulder Creek.
---
