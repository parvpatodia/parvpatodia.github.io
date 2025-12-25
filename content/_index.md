---
# Leave the homepage title empty to use the site title
title: ''
date: 2024-05-01
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  # 1. BIO & EDUCATION SECTION
  - block: resume-biography-3
    # This ID allows the "Bio" tab to scroll here (if linked)
    id: about
    content:
      # CRITICAL FIX: This must match the folder name in content/authors/
      username: admin
      text: ''
      button:
        text: Download CV
        url: uploads/Resume-Parv_Summer_2026.pdf
    design:
      background:
        gradient_mesh:
          enable: true
      avatar:
        size: medium
        shape: circle

  # 2. EXPERIENCE SECTION
  - block: experience
    # This ID allows the "Experience" tab to scroll here
    id: experience
    content:
      title: Experience
      # Date format usually matches what you put in the content files
      date_format: Jan 2006
    design:
      columns: '2'

  # 3. PROJECTS SECTION
  - block: collection
    # This ID allows the "Projects" tab to scroll here
    id: projects
    content:
      title: Projects
      filters:
        # This tells Hugo to pull content from content/projects/
        folders:
          - projects
    design:
      view: article-grid
      columns: '2'

  # 4. RESEARCH / PAPERS SECTION
  - block: collection
    # This ID allows the "Papers" tab to scroll here
    id: publications
    content:
      title: Featured Publications
      filters:
        # This tells Hugo to pull content from content/publications/
        folders:
          - publications
        featured_only: false
    design:
      view: citation
      columns: '2'

  # 5. CONTACT SECTION
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |
        I am currently looking for internship opportunities in AI/ML and Robotics.
      email: patodia.pa@northeastern.edu
      address:
        city: San Jose
        region: CA
        country: United States
    design:
      columns: '2'

  - block: markdown
    content:
      title: '📚 My Research'
      subtitle: ''
      text: |-
        My research focuses on building practical AI systems that solve real-world problems. I work on three main areas: developing ways for multiple computers to learn together without sharing raw data (federated learning), improving how AI models understand and respond to human language more accurately, and creating tools that monitor equipment health before it breaks. Currently, I'm exploring how to make these systems work better with less computing power and less information loss. My goal is to bridge the gap between what researchers develop in labs and what businesses actually need—creating systems that are faster, more reliable, and easier to deploy.

        Please reach out to collaborate 😃
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
---