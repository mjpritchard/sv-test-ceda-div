---
author: Matt Pritchard
title: Welcome to CEDA!
description: The Centre for Environmental Data Analysis serves the environmental science community by the provision of data centres, data analysis & access, and research project participation.
content_blocks:
  - _bookshop_name: hero
    heading:
      title: Welcome to CEDA!
      align: start
      content: >-
        The Centre for Environmental Data Analysis serves the environmental science community by the provision of data centres, data analysis & access, and research project participation.
      width: 6
    align: end
    order: last
    illustration:
      image: img/logos/ceda-ball-logo.png
    links:
      - title: JASMIN
        url: https://jasmin.ac.uk/
        icon: fa-solid fa-computer
        outline: true
      - title: CEDA Archive
        url: https://archive.ceda.ac.uk/
        icon: fa-solid fa-database
        outline: true
    orientation: horizontal
    cover: true
    overlay-mode: dark
    background: 
      backdrop: img/uk-cropped.jpg

  - _bookshop_name: articles
    heading:
      title: Our latest news and updates
    input:
      section: news
      sort: date
    hide-empty: false
    header-style: none
    more:
      title: More news
    padding: 0
    limit: 3
    class: border-0 card-zoom card-body-margin
    justify: center  

  - _bookshop_name: panels
    heading:
      title: Our services
      align: start
    background:
      color: success
      subtle: true
    width: 12
    tab-type: underline
    ratio: 16x9
    elements:
    - title: JASMIN
      image: img/JASMIN.jpg
      content: JASMIN is a globally unique data intensive supercomputer for environmental science. JASMIN supports the data analysis requirements of the UK and European climate and earth system modelling community. It consists of multi-Petabyte fast storage co-located with data analysis computing facilities, with dedicated light paths to various key facilities and institutes within the community. <br> {{< link jasmin >}} **Get started with JASMIN** {{< /link >}}
    - title: The CEDA Archive
      image: img/CEDA-archive.jpg
      content: The CEDA Archive is the national data centre for atmospheric and earth observation and forms part of NERC's Environmental Data Service - a network of data centres covering all aspects of environmental science. Our team coordinate data management on behalf of NERC for the UK atmospheric science and earth observation communities. <br> We hold data covering climate, composition, observations and numerical weather prediction as well as various earth observation datasets, including airborne and satellite data and imagery. Our main goal is to ensure that atmospheric and earth observation data are made available and accessible to all in order to fully realise their reuse potential. <br> {{< link ceda_archive >}} **Explore the data in our archive** {{< /link >}}
    - title: Outreach
      image: img/warming-stripes.png
      content: At CEDA we support environmental scientists coducting climate research. However, you don't need a PhD to get involved! We've designed some resources to help prompt conversations about climate change and highlight things everyone can do to reduce their carbon footprint. <br> {{< link "../outreach" >}} **Find out about our outreach activities and resources** {{< /link >}}
    - title: Other services
      image: img/stock-dish.jpg
      content: CEDA also provide support for numerous other organisations and external projects. We run the {{< link "https://www.ukssdc.ac.uk/" >}} UK Solar System Data Centre (UKSSDC) {{< /link >}} co-funded by STFC and NERC, curates and provides access to archives of data from the upper atmosphere, ionosphere and Earth’s solar environment. The {{< link "https://www.ipcc.ch/" >}} Intergovernmental Panel on Climate Change {{< /link >}}  is the United Nations body for assessing the science related to climate change. We run the {{< link "https://www.ipcc-data.org/" >}} IPCC Data Distribution Centre {{< /link >}}  which provides climate, socio-economic and environmental data, both from the past and also in scenarios projected into the future.

  - _bookshop_name: articles
    heading:
      title: Events
      align: start
    input:
      section: events
      reverse: true
      sort: date
    hide-empty: false
    header-style: none
    more:
      title: More events
    padding: 0
    limit: 3
    class: border-0 card-zoom card-body-margin


  - _bookshop_name: about
    heading:
      title: About us
      content: Our mission is to support environmental science, further environmental data archival practices, and develop and deploy new technologies to enhance access to data. Additionally we provide services to aid large scale data analysis.
        Below you can meet the members of our team, read about the history of our organisation or find out more about our mission!  
      align: start
      width: 8
    background:
      color: primary
      subtle: true
    illustration:
      image: img/CEDA-staff-30th.jpg
    link-type: link
    links:
    - title: Our team
      url: '/about/team.md'
      icon: fa-solid fa-people-group
    - title: Our history
      url: 'about/history.md'
      icon: fa-solid fa-book-open
    - title: Our mission
      url: 'about/mission.md'
      icon: fa-solid fa-rocket
    order: first

  - _bookshop_name: cards
    heading:
      title: Our priorities
      align: start
    background:
      color: info
      subtle: true
    orientation: stacked
    icon-rounded: true
    class: text-center custom-cards
    elements:
    - title: Big data analysis & access
      content: We ensure that atmospheric and earth observation data are made available and accessible to all in order to fully realise their reuse potential. We hold data covering climate, composition, observations and numerical weather prediction as well as various earth observation datasets, including airborne and satellite data and imagery. JASMIN serves the scientific community by providing a range of computing services and supporting a variety of data types in a scalable environment.
      image: img/stock-code.jpg
    - title: Collaboration
      content: JASMIN and the CEDA Archive are shared resources for NERC’s environmental science community, encouraging communication and inter-disciplinary working between diverse scientific groups within the community. This helps to reduce duplication of data, effort and resources. Datasets produced within collaborative workspaces can be identified and passed to the CEDA Archive for curation, discovery and widespread reuse. Most of the Archive is also open to all online users.
      image: img/stock-collaboration.jpg
    - title: Enabling Science
      content: JASMIN and the CEDA Archive enable scientists to carry out research that would not otherwise be possible. This could include monitoring UK biodiversity trends, developing the next generation of climate models, improving our understanding of extreme weather. Or it could even be predicting volcanoes or earthquakes, modeling plant health, and gauging the impact of climate change on food production, amongst many others!
      image: img/stock-fieldwork.jpg

  - _bookshop_name: articles
    heading:
      title: Our projects
    input:
      section: projects
      sort: date
    hide-empty: false
    header-style: none
    more:
      title: More projects
    padding: 0
    limit: 3
    class: border-0 card-zoom card-body-margin
    justify: start 
---
