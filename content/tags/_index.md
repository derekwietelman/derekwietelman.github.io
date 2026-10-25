---
# Don't publish the theme's list pages for this taxonomy (or its terms). No
# paper uses tags, so there's nothing to list.
build:
  render: never
cascade:
  build:
    render: never
    list: always
---
