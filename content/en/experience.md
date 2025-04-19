---
title: 'Experience'
date: '2023-10-24'
type: landing

design:
  spacing: '5rem'

# Note: `username` refers to the user's folder name in `content/authors/`

# Page sections
sections:
  - block: resume-experience
    content:
      username: riad
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: false
  - block: resume-skills
    content:
      title: Skills
      username: riad
    design:
      show_skill_percentage: false
  - block: resume-awards
    content:
      title: Cursos & Certifications
      username: riad
  - block: resume-languages
    content:
      title: Languages
      username: riad
  - block: collection
    id: publications
    content:
      title: Publications
      text: ""
      filters:
        folders:
          - publication
        exclude_featured: false
---