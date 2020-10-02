---
title: Pros and Cons of 11ty
description: This detailes some nice (and not so nice) features of 11ty
layout: base
permalink: /procon/
eleventyNavigation:
  key: Pros/Cons
---
<div class="container">

  # {{title}}

  <br>

  ## Pros of 11ty

  <br>

  - creates static HTML files which are portable and can be shared from user to user easily (via 1 zip file!)
  - very easy to expand your website after initial setup
    - site additions can be made by non-technical people as long as they understand the syntax of markdown (or other templating languages)
  - Easy to replicate / clone sites
  - integrates well with GitHub and can be setup for automatic push/pull when changes are made
  - inherently **secure** because the sites are fully static
  - works with MANY templating languages (I used markdown for this site)

  <br>
    
  ## Cons of 11ty

  <br>

  - utilizes a CLI in order to set up (no GUI)
    - which sucks. It is hard and I had trouble
  - need technical coding experience to understand configuration process
  - designed to be managed by a single user, which means that users cannot collaborate on a single page
  - does not handle dynamic data well (no queries)
  - no interface to work with, just editing .md files
</div>