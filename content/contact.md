---
# Contact page: one card (email, profile links, mailing address, each under its own
# heading) with a photo beside it (block defined in layouts/_partials/hbx/blocks/contact-photo/).
# Photo files go in `assets/media/contact/`.
title: Contact
# Description shown in search results and link previews.
summary: "Email and mailing address for Derek C. Wietelman at CU Boulder's Institute of Behavioral Science, plus Google Scholar, GitHub, LinkedIn, and ResearchGate."
type: landing
# Keep it out of the theme's page list in the phone menu on paper pages.
sidebar:
  hidden: true

sections:
  - block: contact-photo
    id: contact
    content:
      title: Contact
      # Shown under the title. Also keeps Safari from offering to translate this
      # page: it judges the language from the first text on the page, and this
      # page otherwise starts with only the name (which reads as Dutch) and
      # menu words. Keep it a full English sentence ("I'd" reads as Dutch).
      intro: Questions and collaborations are always welcome.
      email_title: Email
      email: derek.wietelman@colorado.edu
      social_title: Find Me On
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
      address_title: Mailing Address
      address:
        - Institute of Behavioral Science
        - University of Colorado Boulder
        - 483 UCB
        - Boulder, CO 80309-0483
      image: contact/boulder-creek.jpg
      image_alt: Boulder Creek flowing between rocky, tree-lined banks
      caption: Taking a lunchtime walk along Boulder Creek.
---
