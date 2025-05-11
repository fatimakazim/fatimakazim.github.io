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

## Observations from Grid 3: A Shift Toward Content-Based Organization

Analyzing Grid 3 revealed a key shift from earlier angle- or perspective-based categorizations to one rooted in content, such as “motifs and flowers,” “animal designs,” “far away,” and “low quality.” This change introduced more variety in the AI’s arrangement and highlighted how visual traits like color and subject matter shaped the grid layout.

![Map](https://drive.google.com/file/d/1hykOyB8v7_7ZS5yqlYzfIUHy4hW10hzm/view?usp=sharing)

The right side of the grid stood out for its dense clustering of decorative panels, especially those with vibrant reds, blues, and greens. These clearly aligned with the “motifs and flowers” category, suggesting the AI responded strongly to visual richness and decorative intensity.

In the middle section, the layout became more mixed. Full truck shots, closeups, and partial views were interspersed without a clear organizing logic, showing how content-based labeling invites a more varied visual distribution compared to angle-based systems.

The left side featured many distant and low-quality images — trucks in broader environmental contexts or small in the frame — aligning with the “far away” and “dull” categories. These images appeared more muted and scattered, reflecting the AI’s difficulty with subjective or spatial categories.

Despite this content shift, color remained a dominant organizing principle. Red panels were grouped together even if labeled under different categories like “closeup” or “motif,” showing the model still leans on aesthetic similarity over semantic distinctions.

Some categories, like “motifs and flowers” and “animal designs,” showed strong, accurate clustering. These culturally rich visuals share distinct shapes and colors, making them easier for the AI to recognize. However, overlap between these categories was also common — for instance, animal designs often resembled floral motifs in composition and tone — which explains the visual blending and cross-classifications.

In contrast, more abstract labels like “far away” and “low quality” were harder for the AI to parse consistently. Their placement often relied more on shared lighting or resolution than the intended category, underlining the challenges of training models to recognize subjective visual cues.


## Exploring VGG-19 vs. InceptionV3

To see how a different algorithm would interpret my dataset of Pakistani truck art, I decided to use VGG-19. I was curious how its visual organization would compare to InceptionV3, which I had tested earlier. While both models worked with the same inputs, their outputs showed some noticeable differences, especially in terms of color grouping, clustering, and layout structure.

With VGG-19, I saw a tighter visual arrangement. On the left side of the grid, there was a dense cluster of decorative panels, especially those with rich reds and blues. These were grouped closely and clearly separated from the central and right sections, which featured full-truck views and environmental shots. VGG-19 seemed to emphasize color and pattern more heavily, grouping images with similar tones and motifs together. This created a sense of visual coherence, where elements like floral designs or symmetrical borders were placed in clear clusters.

In contrast, InceptionV3 offered a looser, more blended layout. While decorative elements were still grouped somewhat, they were often interspersed with side views and truck fronts. The overall structure felt more evenly spread, with softer boundaries between content types. Color and motif similarities were less dominant in its organization, leading to a more fluid visual grid.

## Analysis of Zero-Shot

- Prompt 1: "A truck with vibrant floral motifs and mirrors"

Using a highly descriptive prompt, “a truck with vibrant floral motifs and mirrors” yielded near-perfect confidence scores (ranging from 99.99 to 99.95) across all four images. The model correctly identified trucks from various angles, including side, close-up, and rear views.
What stood out to me was how effective the prompt was when combining multiple specific visual cues. The model clearly performed best when asked to identify distinct features such as “floral motifs” and “bright colors” alongside the object “truck.” This indicates that it benefits from detailed, compound prompts that match its learned visual vocabulary. In contrast, single-word cultural concepts on their own tend to generate weaker results.

- Prompt 2: "Animal"

I was initially skeptical about how well the model would respond to the word “animal,” given how stylized and integrated animal imagery is within truck art. To my surprise, the model identified all the images containing animals with decent accuracy.
However, it became clear that while the model could tell that an animal was present, it had trouble locating or interpreting animals embedded within decorative panels. Images where the animal was more clearly represented received higher scores, while those featuring stylized or symbolic depictions scored zero. This suggests that although the model has been trained on realistic images of animals, it still struggles with abstract or highly stylized representations — a common trait in South Asian decorative arts.

- Prompt 3: "Tyre"

When I used the prompt “tyre,” the model’s performance was especially strong. It accurately pulled images featuring wheels or close-ups of tires, assigning significantly higher confidence scores (1.38, 1.21, 0.52) to the relevant images.
This made it clear that the model is far more confident when identifying mechanical or functional objects, such as tyres, compared to culturally specific motifs. The recognition seems driven by the tire’s distinctive circular form and familiar structure, which are easily mapped to the model’s training data. The contrast in scoring, particularly when compared to more culturally embedded elements, highlights the model’s stronger background in recognizing mechanical features over regional artistic content.


## Analysis of Image Captioning Results

My image captioning results reveal significant limitations in how AI interprets culturally specific visual artifacts.

### - Functional Recognition vs. Cultural Blindness

The first image caption — **"a truck is parked on the side of a road"** — demonstrates how the AI reduces a richly decorated Pakistani truck to its basic utilitarian function.

While technically accurate at identifying the object, it completely overlooks:

- The elaborate hand-painted decorations  
- The cultural significance of the ornamentation  
- The craftsmanship and artistic tradition  

**This illustrates how Western-trained AI prioritizes object identification over cultural context and artistic significance.**

---

### - Visual Misinterpretation

The second caption — **"a colorful picture of a colorful painted wall with a colorful painted flower"** — is particularly revealing:

- Misidentifies truck art **birds** as **flowers**  
- Incorrectly categorizes a **vehicle panel** as a **"wall"**

**This demonstrates the model's tendency to default to generic descriptions when encountering unfamiliar cultural artifacts.**

---

### - Context Elimination

The third caption — **"a man is looking out of a window"** — strips away all cultural specificity:

- Ignores the **ornate decorative framing** typical of Pakistani truck windows  
- Reduces an **artisan's workspace** to a mundane action  
- Misses the **mirror work** and **painted borders** that distinguish this as truck art  

**The AI flattens rich cultural context into universal human activities, erasing what makes truck art distinctive.**

---

### - Complete Misidentification

The fourth caption — **"a man is sitting on a bed with a large stuffed animal"** — reveals the most dramatic failure:

- Completely **misinterprets truck artists at work**  
- **Fabricates non-existent objects** (bed, stuffed animal)  
- Fails to recognize the **creative process of truck art**

**This shows how the model forces unfamiliar visuals into known categories from its training data, leading to absurd results.**

---

### Implications

These results powerfully demonstrate Impett & Offert's observation that _"in reading a corpus of visual culture through a neural network, we are always also doing the reverse."_

The captions reveal:

- The AI’s **Western-centric visual vocabulary** lacks terms for Pakistani artistic traditions  
- A **hierarchy of recognition** where functional objects (truck, window) are prioritized over decorative elements  
- A tendency to **default to familiar contexts** when facing culturally unfamiliar expressions  
- The **erasure of cultural specificity** through generic captioning  
