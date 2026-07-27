<div align="center">

<h1>AIPaperX: A one-stop search engine for top-tier AI conference & Journals papers</h1>


![Hits](https://hits.sh/github.com/ruichen0424/ai-paper-explorer.svg?label=Hits&color=4f46e5)
</div>

## 📝 About The Project

Project Website： [AI Top-Tier Conference & Journal Paper Explorer](https://ruichen0424.github.io/ai-paper-explorer/)

This project aims to systematically collect and organize the published paper metadata from top-tier conferences and journals in Artificial Intelligence (AI), Computer Vision (CV), Natural Language Processing (NLP), and Machine Learning (ML).

To facilitate quick retrieval, statistical analysis, and secondary development for researchers and developers, all paper metadata is archived into folders by **Conference / Journals Name** and subsequently by **Year**. The data is uniformly extracted into a highly readable JSON format.


### 📄 Data Format Specification

Each JSON file represents a collection of papers for a specific conference in a given year. The data is stored in a dictionary (Key-Value) structure for simplicity.


## 📂 Supported Conferences and Journals

This repository currently includes paper data from the following top-tier conferences and journals. The specific details for each folder are as follows:

### Conference

| No. | Name | Folder | Years Covered | Official Data Source | H5-index (Rank) |
|---|---|---|---|---|---|
| 1 | AAAI (AAAI Conference on Artificial Intelligence) | AAAI | 2016 - 2026 | [AAAI Proceedings](https://ojs.aaai.org/index.php/AAAI/issue/archive) | 232 (36) |
| 2 | ACL (Meeting of the Association for Computational Linguistics) | ACL | 2016 - 2026 | [ACL Proceedings](https://aclanthology.org/venues/acl/) | 236 (34) |
| 3 | CVPR (IEEE/CVF Conference on Computer Vision and Pattern Recognition) | CVPR | 2016 - 2026 | [CVF Open Access](https://openaccess.thecvf.com/menu) | 450 (2) |
| 4 | ECCV (European Conference on Computer Vision) | ECCV | 2018 - 2024 (even years) | [ECCV Proceedings](https://www.ecva.net/papers.php) | 262 (22) |
| 5 | EMNLP (Empirical Methods in Natural Language Processing) | EMNLP | 2016 - 2025 | [EMNLP Proceedings](https://aclanthology.org/venues/emnlp/) | 218 (45) |
| 6 | ICCV (IEEE/CVF International Conference on Computer Vision) | ICCV | 2017 - 2025 (odd years) | [CVF Open Access](https://openaccess.thecvf.com/menu) | 256 (25) |
| 7 | ICLR (International Conference on Learning Representations) | ICLR | 2016 - 2026 | [OpenReview](https://openreview.net/group?id=ICLR.cc) | 362 (8) |
| 8 | ICML (International Conference on Machine Learning) | ICML | 2016 - 2026 | [ICML Proceedings](https://proceedings.mlr.press/) | 272 (19) |
| 9 | IJCAI (International Joint Conference on Artificial Intelligence) | IJCAI | 2016 - 2025 | [IJCAI Proceedings](https://www.ijcai.org/all_proceedings) | 136 (-) |
| 10 | NeurIPS (Neural Information Processing Systems) | NeurIPS | 2016 - 2025 | [NeurIPS Proceedings](https://proceedings.neurips.cc/) | 371 (7) |


### Journal

| No. | Name | Folder | Years Covered | Official Data Source | H5-index (Rank) |
|---|---|---|---|---|---|
| 1 | IJCV (International Journal of Computer Vision) | IJCV | 2016 - 2025 | [Springer Nature Link](https://link.springer.com/journal/11263) | 109 (-) |
| 2 | TIP (IEEE Transactions on Image Processing) | TIP | 2016 - 2025 | [IEEE Xplore](https://ieeexplore.ieee.org/xpl/mostRecentIssue.jsp?punumber=83) | 165 (-) |
| 3 | TNNLS (IEEE Transactions on Neural Networks and Learning Systems) | TNNLS | 2016 - 2025 | [IEEE Xplore](https://cis.ieee.org/publications/t-neural-networks-and-learning-systems) | 165 (-) |
| 4 | TPAMI (IEEE Transactions on Pattern Analysis and Machine Intelligence) | TPAMI | 2016 - 2025 | [IEEE Xplore](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=34) | 217 (46) |


## 🛠️ Quick Start

You can directly download the corresponding JSON files and easily parse them using Python:

``` python
import json

# Load CVPR 2026 paper data
with open('./CVPR/cvpr_2026.json', 'r', encoding='utf-8') as f:
    papers = json.load(f)

# Print the first 5 papers
for paper in papers[:5]:
    print(f'Title: {paper["title"]}\nURL: {paper["url"]}\n')
```

## 📜 Disclaimer & License

This project only crawls and organizes publicly available, factual metadata (titles and public links) of academic papers. It does not contain full texts or abstracts protected by copyright. The final interpretation rights of all data belong to the official committees of the respective conferences and journals.