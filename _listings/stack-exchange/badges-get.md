---
swagger: "2.0"
info:
  title: Stack Exchange Get Badges
  description: "Returns all the badges in the system.\n \nBadge sorts are a tad complicated.
    For the purposes of sorting (and min/max) tag_based is considered to be greater
    than named.\n \nThis means that you can get a list of all tag based badges by
    passing min=tag_based, and conversely all the named badges by passing max=named,
    with sort=type.\n \nFor ranks, bronze is greater than silver which is greater
    than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver
    for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n
    \nThis method returns a list of badges."
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /badges:
    get:
      summary: Get Badges
      description: Returns all the badges in the system
      operationId: returns-all-the-badges-in-the-system-badge-sorts-are-a-tad-complicated-for-the-purposes-of-sorting-a
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: |-
          #Discussion

          The Stack Exchange API allows applications to exclude almost every field returned
      - in: query
        name: fromdate
        description: Unix date
      - in: query
        name: inname
      - in: query
        name: max
        description: |
          sort = rank => string
          sort = name => string
          sort = type => string
      - in: query
        name: min
        description: |
          sort = rank => string
          sort = name => string
          sort = type => string
      - in: query
        name: order
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      - in: query
        name: sort
      - in: query
        name: todate
        description: Unix date
      responses:
        200:
          description: OK
      tags:
      - badges
definitions:
  created_comment:
    properties:
      body:
        description: This is a default description.
        type: get
      body_markdown:
        description: This is a default description.
        type: get
      can_flag:
        description: This is a default description.
        type: get
      comment_id:
        description: This is a default description.
        type: get
      creation_date:
        description: This is a default description.
        type: get
      edited:
        description: This is a default description.
        type: get
      link:
        description: This is a default description.
        type: get
      owner:
        description: This is a default description.
        type: get
      post_id:
        description: This is a default description.
        type: get
      post_type:
        description: This is a default description.
        type: get
  error:
    properties:
      error_id:
        description: This is a default description.
        type: get
      error_message:
        description: This is a default description.
        type: get
      error_name:
        description: This is a default description.
        type: get
  info_object:
    properties:
      answers_per_minute:
        description: This is a default description.
        type: get
      api_revision:
        description: This is a default description.
        type: get
      badges_per_minute:
        description: This is a default description.
        type: get
      new_active_users:
        description: This is a default description.
        type: get
      questions_per_minute:
        description: This is a default description.
        type: get
      site:
        description: This is a default description.
        type: get
      total_accepted:
        description: This is a default description.
        type: get
      total_answers:
        description: This is a default description.
        type: get
      total_badges:
        description: This is a default description.
        type: get
      total_comments:
        description: This is a default description.
        type: get
  single_filter:
    properties:
      filter:
        description: This is a default description.
        type: get
      filter_type:
        description: This is a default description.
        type: get
      included_fields:
        description: This is a default description.
        type: get
  user:
    properties:
      about_me:
        description: This is a default description.
        type: get
      accept_rate:
        description: This is a default description.
        type: get
      account_id:
        description: This is a default description.
        type: get
      age:
        description: This is a default description.
        type: get
      answer_count:
        description: This is a default description.
        type: get
      badge_counts:
        description: This is a default description.
        type: get
      creation_date:
        description: This is a default description.
        type: get
      display_name:
        description: This is a default description.
        type: get
      down_vote_count:
        description: This is a default description.
        type: get
      is_employee:
        description: This is a default description.
        type: get
x-collection-name: Stack Exchange
x-streamrank:
  polling_total_time_average: "0.17"
  polling_size_download_average: "167.5"
  streaming_total_time_average: "0.12"
  streaming_size_download_average: "84.38"
  change_yes: "887"
  change_no: "935"
  time_percentage: "29"
  size_percentage: "50"
  change_percentage: "49"
  last_run: "2018-05-01"
  days_run: "1"
  minute_run: "0"
---