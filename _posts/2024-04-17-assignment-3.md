---
title: "Assignment 3"
categories:
  - Blog
tags:
  - Post Formats
  - quote
---

#  Pakistani Truck Art: AI Interpretation and Cultural Analysis
For this project, I chose to explore Pakistani truck art, which is a vibrant and culturally rich tradition that has fascinated me since childhood. Growing up, I was always captivated by the striking visuals of trucks adorned with intricate patterns, portraits of celebrities, animals, calligraphy, and poetic quotes. This unique, hyper-localized form of expression made me curious: how would an AI model interpret and categorize such a distinctly regional art form?

## Grid 1: No Categories
To begin, I curated a dataset of 105 images sourced from Getty Images. For the initial cluster analysis, I deliberately avoided pre-sorting the images into folders. Instead, I fed the entire dataset into Orange Data Mining to observe how the AI would organically group the visuals.
![Map](https://drive.google.com/file/d/1cnthZ5gGb-q-FKdoF0RTKIPS6d4Cck8p/view?usp=sharing)

- On the right side, the AI grouped images with detailed art panels, particularly those featuring geometric and floral designs.

- The left and center clusters leaned toward full truck views and environmental context shots.
The image grid revealed natural clustering patterns:

Despite the lack of explicit categories, the AI exhibited some pattern recognition based on color schemes and decorative styles. However, without labeled data, it struggled to produce nuanced classifications.
I then applied hierarchical clustering to examine the data in more depth. This approach revealed clearer and more distinct groupings, which I further explored using the image viewer.

## Grid 2:  Perspective-Based Categorization of Pakistani Truck Art
- For the second categorization, I manually sorted the dataset into four folders based on visual perspective: side view, front view, tyre, and detailed art—with the latter consisting of close-up shots highlighting the intricate designs painted on the trucks.
![Map](https://drive.google.com/file/d/1DRJh6MyAJ6nfu2JQdcUx_eLuCZSVNTKO/view?usp=sharing)

Once processed through the AI model, the image grid revealed some clear visual organization patterns. Notably, there was strong clustering by decorative style, particularly on the left side of the grid, where detailed art panels featuring geometric and floral patterns were grouped closely—often organized by dominant colors such as reds, blues, and greens. The central and right portions of the grid mostly contained full truck views, organized loosely by shooting angle. Meanwhile, tyre close-ups appeared primarily along the bottom row, though they were more scattered and lacked the tight coherence of other categories.

![Map](https://drive.google.com/file/d/1KpPsEuWxxlbOJR14A8V9xNmk-lnzOhf3/view?usp=sharing)

### AI Interpretation Insights

From an AI interpretation standpoint, it became clear that the model prioritized visual features like color and pattern over the semantic categories I had defined. For example, similarly colored art panels were tightly clustered regardless of whether they came from side, front, or detail shots. While there was some success in grouping similar viewing angles—such as front and side views—the AI often ignored these distinctions when decorative features were more visually prominent. This was especially evident in the misclassification of tyre images, which showed poor clustering and were supported by a confusion matrix accuracy of only 25%, indicating the model struggled to treat “tyre” as a distinct visual category. In contrast, the detailed art category showed strong visual coherence and performed best, achieving an accuracy of 88.9%.


