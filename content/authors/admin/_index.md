Based on the Netlify build log you provided, the website build failed due to a YAML parsing error in the `_index.md` file.

### **Analysis of the Error**

The error message `failed to unmarshal YAML: yaml: line 15: did not find expected key` points to a syntax problem in the file's front matter. While the error is reported at line 15, the actual cause is often an incorrect data structure earlier in the file that misleads the YAML parser.

The specific issue was that the `languages` information was incorrectly nested within the `skills` section. The website theme expects `languages` to be a distinct, top-level category, at the same level as `education`, `work`, and `skills`.

### **Corrected `_index.md` File**

Here is the corrected version of the `_index.md` file. It has been updated with the information from your CV and the YAML structure has been fixed to resolve the build error.

```markdown
---
# Display name
title: Rahat Aayaz

# Full name (for SEO)
first_name: Rahat
last_name: Aayaz

# Status emoji
status:
  icon: ☕️

# Is this the primary user of the site?
superuser: true

# Role/position/tagline
role: Research Assistant

# Organizations/Affiliations to display in Biography blox
organizations:
  - name: Khulna University of Engineering & Technology (KUET)
    url: https://www.kuet.ac.bd/

# Social network links
profiles:
  - icon: at-symbol
    url: 'mailto:rahataayaz@gmail.com'
    label: E-mail Me
  - icon: brands/google-scholar
    url: https://scholar.google.com/citations?user=qqBA5UMAAAAJ&hl=en
    label: Google Scholar
  - icon: brands/github
    url: https://github.com/Rahataah
    label: GitHub
  - icon: brands/linkedin
    url: https://www.linkedin.com/in/rahat-aayaz-1b1a7b20a/
    label: LinkedIn
  - icon: brands/orcid
    url: https://orcid.org/0009-0009-9641-8033
    label: ORCID

education:
  - area: Bachelor of Science in Engineering
    institution: Khulna University of Engineering & Technology
    date_start: 2018-12-01
    date_end: 2024-03-31
    summary: |
      [cite_start]Department: Building Engineering and Construction Management [cite: 5]
      [cite_start]Major: Structural & Materials Engineering [cite: 5]
      [cite_start]CGPA: 3.14/4.00 [cite: 5]
  - area: Higher Secondary Certificate (HSC)
    institution: Birshreshtha Noor Mohammad Public College
    date_start: 2016-03-01
    date_end: 2018-04-30
    [cite_start]summary: 'Field of study: Science [cite: 5]'
  - area: Secondary School Certificate (SSC)
    institution: Faizur Rahman Ideal Institute
    date_start: 2006-01-01
    date_end: 2016-02-29
    [cite_start]summary: 'Field of study: Science [cite: 5]'

work:
  - position: Research Assistantship
    company_name: Khulna University of Engineering & Technology (KUET)
    company_url: 'https://www.kuet.ac.bd/'
    date_start: 2024-03-01
    date_end: ''
    summary: |
      [cite_start]Department of Building Engineering and Construction Management. [cite: 3]
      [cite_start]Responsibilities: Research Article Drafting and Analysis, Lab Instruction, Machine Learning Analysis, Structural Designing. [cite: 3]
  - position: Undergraduate Thesis
    company_name: Khulna University of Engineering & Technology (KUET)
    company_url: 'https://www.kuet.ac.bd/'
    date_start: 2023-01-01
    date_end: 2024-02-28
    [cite_start]summary: 'Thesis Title: Enhancing High-Strength Concrete Incorporating Graphene and Hybrid Fibers: A Multi-Layered Laboratory Experiments and Machine Learning Analysis [cite: 3]'

skills:
  - name: Technical Skills
    items:
      - name: Structural Analysis (ETABS, Robot, STAAD.Pro)
        description: ''
        percent: 0
      - name: Finite Element Analysis (ANSYS, Abaqus)
        description: ''
        percent: 0
      - name: CAD & BIM (AutoCAD, Revit, Navisworks)
        description: ''
        percent: 0
      - name: Programming (Python, C++, MATLAB)
        description: ''
        percent: 0
      - name: Architectural Visualization (Lumion, Twin Motion)
        description: ''
        percent: 0

languages:
  - name: Bangla
    percent: 100
  - name: English
    percent: 90

awards:
  - title: Unsupervised Learning, Recommenders, Reinforcement Learning
    date: '2024-10-01'
    awarder: Coursera (offered by Stanford University)
    icon: coursera
    [cite_start]summary: 'Skills: Unsupervised learning techniques (K-Means, PCA, Hierarchical Clustering), Recommender systems (Collaborative Filtering, Matrix Factorization), Reinforcement learning (Q-learning, MDPs). [cite: 33]'
  - title: Advanced Learning Algorithms
    date: '2024-08-01'
    awarder: Coursera (offered by Stanford University)
    icon: coursera
    [cite_start]summary: 'Skills: Deep learning architectures (CNNS, RNNS, LSTMs), Advanced optimization techniques, Unsupervised learning (GMMs, PCA), TensorFlow/PyTorch implementation. [cite: 35]'
  - title: Supervised Machine Learning - Regression and Classification
    date: '2024-06-01'
    awarder: Coursera (offered by Stanford University)
    icon: coursera
    [cite_start]summary: 'Skills: Linear and logistic regression, classification algorithms, model training and evaluation, bias-variance tradeoff, feature engineering, regularization techniques (L1, L2), and Python programming for ML. [cite: 36]'
  - title: Technical Support Fundamentals
    date: '2024-01-01'
    awarder: Coursera (offered by Google)
    icon: coursera
    [cite_start]summary: 'Skills: Troubleshooting and Problem Solving, Operating System Basics, Networking Fundamentals, Command Line Interface (CLI) Proficiency. [cite: 37]'
  - title: Financial Markets
    date: '2020-10-01'
    awarder: Coursera (offered by Yale University)
    icon: coursera
    [cite_start]summary: 'Skills: Understanding Financial Markets and Instruments, Risk Management and Behavioral Finance, Investment Strategies and Portfolio Management, Market Regulation, Historical Financial Crises. [cite: 38]'
---

[cite_start]I am a Research Assistant at the Department of Building Engineering and Construction Management at Khulna University of Engineering & Technology (KUET)[cite: 3]. [cite_start]My research focuses on sustainable and high-performance construction materials, including the development of high-strength concrete using graphene and hybrid fibers[cite: 3, 8]. [cite_start]I specialize in applying machine learning techniques to predict and optimize the properties of concrete, utilizing SHAP and PDP analysis for advanced model interpretation[cite: 10, 14, 15, 21].

[cite_start]I have authored and co-authored several research articles in peer-reviewed journals, including Elsevier's *Journal of Materials Research and Technology* [cite: 8][cite_start], *Construction & Building Materials* [cite: 11][cite_start], and *Cleaner Engineering and Technology*[cite: 13]. [cite_start]Additionally, I have presented my research at international conferences such as ICCESD 2024[cite: 18].
```
