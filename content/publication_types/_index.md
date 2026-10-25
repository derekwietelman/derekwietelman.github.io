---
# Don't publish the theme's list pages for this taxonomy (or its terms); the
# Research page still uses the taxonomy internally to sort papers into its lists.
build:
  render: never
cascade:
  build:
    render: never
    list: always
---
