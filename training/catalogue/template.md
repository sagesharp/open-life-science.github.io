---
layout: page
title: TOPIC Training Modules
description: TOPIC training modules offered by Open Life Science.
topic: TOPIC - e.g. "Open Data" -- make sure the topic name is unique across all topics, or the anchor links to different topics on the catalogue page won't work.
motivation: Why would someone want to study this topic? (Not what they will study)
customization: (optional) Pitch to [customize our training modules to fit your needs](/training/training-services). If you delete this line, a default customization sentence will be used.
topic-image: (optional) HTML link to image, or location in source tree
topic-image-alt: (optional, but must be included if you add topic-image) Alternate text - description of image. Optionally include license and artist attributions.
modules:
    -
        title: Module Title -- make sure each module title is unique within a training topic, or the anchor links to different modules on the topic page won't work.
        description: Description of course. Multiple sentences in one longer paragraph. This one line will be included in the training catalogue page after the module title, so keep this short. Paragraph breaks or markdown will not be displayed properly.
        count-this-module: true - If you want this module to be counted in the total number of modules on the training catalog page, write 'true'. Some times you don't want the module to be counted in the total because it's a cohort presentation call and not a training module. In that case, you would write 'false'. If you're listing two modules with the same topic to show how modules can be customized for different audiences, one module would be marked as 'true' and the other module would be marked as 'false'
        learning-goals: |
            (Optional) Write in markdown format the learning goals.
        prework: |
            (Optional) Write in markdown format any instructions for prework.
        video:
            speakers:
            - (optional) username of speaker -- check _data/openseeds/library.yaml for this
            recording: HTML link - expected in the form https://youtu.be/videostring?t=268
            date: 2020-11-05
            transcript: (optional) HTML link
            slides: (optional) HTML link
            citation-text: (optional) One line text sentence of citation, no markdown formatting allowed.
            citation-link: (optional) HTML link
            program-name: (optional) Program name, with no acronyms so that an outsider understands it. E.g. "Open Seeds cohort 2"
            program-link: (optional, but must be included with program-name) HTML link to program, e.g. https://we-are-ols.org/openseeds/ols-2/
            resources: |
                (optional) Markdown formatted links to resources. E.g.

                [Data Readiness Group](https://datareadiness.eng.ox.ac.uk/)

                [2016 article on FAIR data practices](https://www.nature.com/articles/sdata201618) - Wilkinson, M., Dumontier, M., Aalbersberg, I. et al. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data 3, 160018 (2016). [https://doi.org/10.1038/sdata.2016.18](https://doi.org/10.1038/sdata.2016.18)
    -
        title: FAIR Data - Insights and Perspectives
        description: Description of course. Multiple sentences in one longer paragraph.
        count-this-module: true
        video:
            speakers:
            - proccaserra
            recording: https://youtu.be/ylqDx_ELfus?t=268
            date: 2020-11-05
            transcript: https://www.example.com
            slides: https://docs.google.com/presentation/d/1ER_ZQ_Fe_PFWBPrP87dU6jRaPT2dlB4hCu-wGXJwnBA/edit?usp=sharing
            citation: https://tess.elixir-europe.org/events/open-life-science
            program-name: Open Seeds cohort 2
            program-link: https://we-are-ols.org/openseeds/ols-2/
            resources: |
                [Data Readiness Group](https://datareadiness.eng.ox.ac.uk/)

                [2016 article on FAIR data practices](https://www.nature.com/articles/sdata201618) - Wilkinson, M., Dumontier, M., Aalbersberg, I. et al. The FAIR Guiding Principles for scientific data management and stewardship. Sci Data 3, 160018 (2016). [https://doi.org/10.1038/sdata.2016.18](https://doi.org/10.1038/sdata.2016.18)
        learning-goals: |
            During this lesson, you will learn:

             - This thing.
             - Another thing.
             - Yet another thing.
        prework: |
            1. [Download this data file](https://www.example.com)
            2. [Install this data processing software](https://www.example.com)


---


{% include _includes/training-module.md %}