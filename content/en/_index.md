---
# Leave the homepage title empty to use the site title
title: "Ríad M. Nassiffe"
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: riad
      text: ""
      # Show a call-to-action button under your biography? (optional)
      # button:
      #   text: Download CV
      #   url: uploads/resume.pdf
    design:
      css_class: light
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
  - block: features
    id: skills
    content:
      title: Main Skills
      text: 
      items:
        - icon: devicon/salesforce
          name: 
          description: Current working!
        - icon: devicon/git
          name: 
          description: Current working!
        - icon: devicon/linux
          name: 
          description: Linux user since 2006.
        - icon: arrow-trending-up
          name: Optimization
          description: Discrete and continuous (convex and piecewise linear) optimization problems.
        - icon: devicon/python
          name: 
          description: Pygames, Flask, Django, scipy, cvxpy and ...
        - icon: devicon/c
          name: 
          description: Optimization algorithms
        - icon: devicon/java
          name:  
          description: Web develper in java on 2008.
        - icon: camera
          name:  
          description: My travels :)
      # Choose a user profile to display (a folder name within `content/authors/`)
      # username: riad
      # # Choose a layout view
      # text: ""
    design:
      css_class: 'featurette-icon'
  - block: collection
    id: post
    content:
      title: Posts
      subtitle: ''
      text: ''
      # Page type to display. E.g. post, talk, publication...
      page_type: post
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: article-grid
      columns: '3'
      css_class: light
      background:
        color: WhiteSmoke
  - block: collection
    id: projects
    content:
      title: Projects
      text: 
      filters:
        folders:
          - project
    design:
      view: article-grid
      fill_image: true
      columns: '2'
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
      css_class: light
      background:
        color: WhiteSmoke
---