---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "A Simple Framework for Cross-Domain Few-Shot Recognition with Unlabeled Data"
authors: [A Islam, R Chen, R Panda, L Karlinksky, RJ Radke, RS Feris]
date: 2021-04-15
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2021-06-15

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops"
publication_short: "CVPRW"

abstract: "Most existing works in few-shot learning rely on meta-learning the model on a large base dataset which is typically from the same domain as the target dataset. We tackle the problem of cross-domain few-shot learning where there is a large shift between the base and target domain. We propose a simple solution to utilize unlabeled images from the novel/base dataset. We calculate pseudo soft-label from the weakly-augmented version of the unlabeled image and compare it with the strongly augmented version. We also minimize the supervised cross-entropy loss for the labeled base dataset at the same time. We show that the proposed network learns representation that can be easily adapted to the target domain even though it has not been trained with target-specific classes during the pretraining phase. Our model outperforms the current state-of-the art method by 2.7% for 5-shot and 3.6% for 1-shot classification in the BSCD-FSL benchmark."

# Summary. An optional shortened abstract.
summary: "We tackle the problem of cross-domain few-shot learning where there is a large shift between the base and target domain. We propose a simple solution to utilize unlabeled images from the novel/base dataset by calculating pseudo soft-label from the weakly-augmented version of the unlabeled image and compare it with the strongly augmented version. Our model outperforms the current state-of-the art method by 2.7% for 5-shot and 3.6% for 1-shot classification in the BSCD-FSL benchmark."

tags: []
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: 
url_code:
url_dataset:
url_poster: 
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: "Right"
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
