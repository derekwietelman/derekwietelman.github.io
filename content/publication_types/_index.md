---
# Don't publish the theme's list pages for this taxonomy (or its terms); the
# homepage still uses the taxonomy internally to sort papers.
build:
  render: never
cascade:
  build:
    render: never
    list: always
---
