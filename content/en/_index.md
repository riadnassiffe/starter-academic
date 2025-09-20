---
# Leave the homepage title empty to use the site title
title: "Ríad M. Nassiffe"
date: '2022-10-24'
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      username: riad
      text: ""
      # Show a call-to-action button under your biography? (optional)
      # button:
      #   text: Download CV
      #   url: uploads/resume.pdf
    design:
      # css_class: light
      background:
        # color: black
        image:
          # Add your image background to `assets/media/`.
          filename: IMG_7916.JPG
          filters:
            brightness: 1.0
          size: cover
          position: left
          parallax: true
  - block: collection
    id: post
    content:
      title: 'Posts'
      subtitle: ''
      page_type: post
      count: 5
      filters:
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      offset: 0
      order: desc
    design:
      view: article-grid
      columns: '3'
      css_class: light
  - block: collection
    id: projects
    content:
      title: 'Projects'
      filters:
        folders:
          - project
    design:
      view: article-grid
      fill_image: true
      columns: '2'
  - block: collection
    id: teachings
    content:
      title: 📚 Teachings
      text: This section will have text in Portuguese, due to the courses are happening in Portuguese.
      filters:
        folders:
          - teachings
    design:
      view: article-grid
      fill_image: true
      columns: '2'
      # background:
      #   color: WhiteSmoke
  - block: collection
    id: publications
    content:
      title: Publications
      text: ""
      filters:
        folders:
          - publication
    design:
      view: citation
      fill_image: true
      columns: '3'
    # design:
    #   # view: citation
    #   css_class: light
    #   background:
    #     color: WhiteSmoke
---