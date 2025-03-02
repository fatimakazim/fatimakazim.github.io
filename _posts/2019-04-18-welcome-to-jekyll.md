---
title: "Assignment 1: How Feminist Ideas Evolved"
description: "A Textual Analysis of Gender, Oppression, and Identity By Fatima and Ghadir"
date: 2019-04-18T15:34:30-04:00
categories:
  - blog
tags:
  - digital Humanities
  - update
---

## Introduction
Feminist ideas have changed a lot over time, influenced by the historical and social challenges of each era. This study looks at three important feminist texts: *A Vindication of the Rights of Woman* (1792) by Mary Wollstonecraft, *The Second Sex* (1949) by Simone de Beauvoir, and *Ain’t I a Woman: Black Women and Feminism* (1981) by Bell Hooks. Each of these books pushes back against the way society defines women, but they do so in different ways. Wollstonecraft, writing in the 18th century, argues that women are not naturally inferior but are kept in a lower position because they are denied education and opportunities (Wollstonecraft). She believed women should be seen as rational individuals, just like men. Over 150 years later, Beauvoir introduced the idea that womanhood is not something women are born into, but something society forces upon them, showing how women have been treated as the "Other" in a world designed for men (Beauvoir 267; Moi). Then, in the late 20th century, Hooks took feminism further by exposing its failure to address race and class, arguing that Black women experience oppression differently because they face both racism and sexism (Hooks). Looking at these three books together, we can see how feminist ideas have expanded, from fighting for basic rights like education to questioning what it even means to be a woman and addressing the larger power structures that shape oppression. Over time, feminism has become more complex and inclusive, reflecting the diverse struggles women have faced across history.

## Methodology
We conducted a computational analysis using Voyant Tools and R Markdown, generating four key visualizations: a word cloud, a word frequency table, a TF-IDF analysis table, and a word frequency graph. After loading the necessary packages, we combined the three texts into a single data frame, tokenized the text, and removed stop words for accuracy. Using `count(word, sort = TRUE)`, we identified the most frequent words and visualized them in a word cloud. The `bind_tf_idf(word, source, n)` function computed the TF-IDF scores to highlight distinctive words in each text. Finally, we created a word frequency graph to compare linguistic patterns across the three works.

![Word Cloud](https://raw.githubusercontent.com/fatimakazim/fatimakazim.github.io/master/assets/images/wordcloud.png)



## Analysis and Findings
For the first part of the analysis, we used Voyant Tools to explore the language in *A Vindication of the Rights of Woman*, *The Second Sex*, and *Ain’t I a Woman*. We looked at word frequency, common phrases, and how key terms are linked to see how each author discussed gender, oppression, and womanhood. In the visualizations, the key terms appear in blue, with larger words representing the most frequently used terms in each text. Additionally, the thicker the line connecting two words, the stronger their relationship, meaning they often appear together in the text. This helped us track changes in feminist thought over time. For example, Wollstonecraft often focused on reason, Beauvoir on otherness, and Hooks on race and intersectionality. By studying these connections, we gained insight into how feminist ideas have evolved across different historical periods.

<iframe style='width: 426px; height: 592px;' src='https://voyant-tools.org/tool/CollocatesGraph/?query=home*&query=home&query=life&query=men&query=women&query=man&query=children&corpus=8abd612db5621971ff1faa824465e2ad'></iframe>

Mary Wollstonecraft’s *A Vindication of the Rights of Woman* criticizes the rules and traditions that limit women’s roles in society. The word “women” is central in her argument and is closely connected to “men,” “society,” “life,” and “duties,” showing her belief that social norms hold women back from getting an education, being independent, and having equal rights. She explains how “men” are seen as the leaders in both public life and at home, while words like “children” and “wives” reinforce the idea that women are expected to be caretakers instead of intellectual equals. Wollstonecraft challenges the belief that a woman’s main purpose is to be a wife and mother. The link between “men” and “society” shows her criticism of male-led institutions that keep women in lower positions. The connection between “life” and “women” highlights her call for women to have control over their own lives. Her work is a key feminist argument for changing social structures and giving women more freedom and equality.

<iframe style='width: 709px; height: 411px;' src='https://voyant-tools.org/tool/CollocatesGraph/?query=father&query=father*&query=home&corpus=58f6970aeb658858f8f3eb91ab456c49'></iframe>

Simone de Beauvoir’s *The Second Sex* critiques how women have historically been defined in relation to men rather than as independent individuals. The central focus on “woman” and its strong link to “man” reflects her argument that gender roles are socially constructed. She explores how marriage and family life confine women, with terms like “mother,” “wife,” and “home” emphasizing traditional domestic expectations. Beauvoir also critiques patriarchal authority, with “man” linked to “authority” and “God,” reinforcing the idea that men are positioned as the societal norm while women are the “Other.” Through these themes, Beauvoir argues that women’s liberation depends on breaking free from restrictive social roles and achieving true autonomy.

<iframe style='width: 890px; height: 509px;' src='https://voyant-tools.org/tool/CollocatesGraph/?query=racism&query=slave&query=feminism*&corpus=896ae0f748615b1d733b55e735325492'></iframe>

Bell Hooks’ *Ain’t I a Woman: Black Women and Feminism* focuses on how race and gender shape women’s experiences. The most important words in her text (“black,” “white,” and “women”) show that she examines how racism and sexism are connected. The strong link between “black” and “white” suggests she discusses racial identity, privilege, and exclusion in feminism, while “women” being connected to both highlights her intersectional approach. Though “men” and “male” appear, they are less central, meaning patriarchy is discussed but not the main focus. The words “slave,” “black,” “women,” and “experience” being connected show how the history of slavery still affects Black women. The presence of “racism” and “sexism” emphasizes that these struggles overlap, and “sexual” being linked to “white” and “women” suggests a discussion of sexual politics and exploitation. The word “feminism” shows that Hooks critiques the feminist movement, and “experience” being tied to “woman” and “slave” reinforces her argument that lived experiences matter in feminist discussions. Overall, Hooks challenges feminism’s failure to fully include Black women and calls for a more inclusive, intersectional movement.

![TF-IDF Table](https://raw.githubusercontent.com/fatimakazim/fatimakazim.github.io/master/assets/images/IDF.table.png)

The TF-IDF analysis highlights key terms that reveal how each author constructs womanhood. In Bell Hooks' text, high TF-IDF values for words related to racism and sexism emphasize intersectionality, showing that she frames womanhood through systems of oppression. Terms like movement (TF-IDF: 0.0021) and feminist (TF-IDF: 0.0013) suggest a focus on activism, reinforcing her view that feminism must address race and class to be truly inclusive. The presence of labor and roles further underscores her emphasis on economic and social structures shaping women’s lives.
Beauvoir’s text includes words like mme (Madame) and ff, which likely relate to women’s social status in a patriarchal framework. While these terms have lower TF-IDF scores, they reinforce her argument that language and labels shape perceptions of women. Her focus on womanhood as a social construct is reflected in how these terms appear in discussions of societal expectations.

Wollstonecraft’s text, on the other hand, includes words like whilst and duties, reflecting an 18th-century discourse on women’s roles, particularly in relation to morality and obligation. Her emphasis on duties aligns with her argument that women's position in society is largely determined by their education and moral responsibilities. 


![Word Graph](https://raw.githubusercontent.com/fatimakazim/fatimakazim.github.io/master/assets/images/frequency%20graph.png)
The graphs compare word usage between the three texts. In the graph comparing Simone de Beauvoir and bell hooks, the words most frequently used by Hooks are male, female, power, American, Black, feminist, and power. The presence of "Black" and "American" suggests that national and racial identity are central to her feminist critique, which aligns with her focus on intersectionality. The repetition of “power” suggests that Hooks’s work is primarily about power structures. She is interested in how gender, race, and nationality intersect to shape power dynamics. Compared to Beauvoir and Wollstonecraft, she is more explicitly concerned with structural oppression and intersectionality rather than individual agency or moral virtue.

Simone de Beauvoir's most used words are feels, abandon, body, love, and girl. The dominance of “feels” and “love” suggests that Beauvoir’s work is highly subjective and psychological—she is interested in how women experience oppression internally. The words “abandon” and “girl” suggest a focus on socialization—how girls are conditioned to be dependent, emotional, and secondary to men. Beauvoir’s feminism is about how women come to understand themselves—the existential crisis of being reduced to one’s body, emotions, and relationships rather than being recognized as a fully autonomous subject. Unlike Hooks, who focuses on power structures, Beauvoir is concerned with how women internalize oppression and struggle to break free from it.

Lastly, for Mary Wollstonecraft, her most frequent words include character, affection, advice, and abilities. The emphasis on “character” and “abilities” suggests that Wollstonecraft is focused on women’s moral and intellectual development. The presence of “Advice” indicates that her text is prescriptive, offering solutions to improve women’s status through education and rational thought. “Affection” also stands out because it implies that Wollstonecraft is still engaging with the 18th-century traditional expectations of women as emotional beings, even if she is trying to redefine what that means. Thus, what the word frequency suggests about her central themes is that Wollstonecraft’s feminism is about educational and moral uplift. She believes that women can and should improve themselves through reason and virtue rather than remain trapped in shallow roles dictated by emotions. Unlike Hooks, who critiques power structures, and Beauvoir, who explores subjective experience, Wollstonecraft offers a roadmap for self-improvement and intellectual equality.

## Discussion
Conducting computer-generated analysis was an eye-opening experience. While we had a general understanding of the texts—their authors, historical contexts, and themes—distant reading and computational analysis helped uncover distinct patterns and differences between them. Moretti’s concept of "distant reading" provides an insightful framework for this process. He distinguishes it from traditional "close reading," suggesting that with large datasets, we must step back to see the bigger picture, revealing relationships and structures that would otherwise be hidden.
In our analysis, this shift allowed us to observe how different authors’ vocabulary reflected the evolution of feminist discourse over time. Initially, we expected a significant overlap in word usage due to the shared themes of feminism and women’s rights. However, the specific words used by each author highlighted different approaches to womanhood. From Wollstonecraft’s focus on morality and education to Beauvoir’s existentialist perspective and Hooks’s intersectional critique, we saw the shifting priorities of feminist thought across centuries.
This process also made us more aware of the limitations of computational text analysis. As Kirmizialtin and Wrisley (2024) note in Exploring Gulf Manumission Documents with Word Vectors, errors in text recognition can skew results, and methods like word vector analysis, though powerful, don't always capture the full complexity of meaning. Similarly, word clouds can misrepresent meaning by treating frequent words equally without considering relationships, making critical interpretation of computational findings necessary.


## Conclusion
Our analysis of A Vindication of the Rights of Woman, The Second Sex, and Ain’t I a Woman gave us a deeper understanding of how feminist ideas have changed over time. By using Voyant Tools and R Markdown, we were able to see patterns in how each author talks about womanhood. While these tools helped highlight key themes and trends, they also showed the limits of distant reading, since word frequency alone can’t fully capture meaning without context. 

## References 

- Beauvoir, Simone de. *The Second Sex*. Translated by Constance Borde and Sheila Malovany-Chevallier, Vintage, 2011.  
- hooks, bell. *Ain’t I a Woman: Black Women and Feminism*. South End Press, 1981.  
- Moi, Toril. *Simone de Beauvoir: The Making of an Intellectual Woman*. Oxford UP, 2008.  
- Wollstonecraft, Mary. *A Vindication of the Rights of Woman*. Edited by Janet Todd, Oxford UP, 2008.  
- Rockwell, Geoffrey, and Stefan Sinclair. "False Positives: Opportunities and Dangers in Big-Data Text Analysis." *Hermeneutica*, 2016, p. 113.  
- Kirmizialtin, Suphan, and David Joseph Wrisley. "Exploring Gulf Manumission Documents with Word Vectors." *Journal of Digital Islamicate Research*, vol. 2, 2024, pp. 1–29.



```


