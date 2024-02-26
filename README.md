# PPP-dataset
Data and code release for PPP paper

本项目提供的SCOPUS数据库与PATSTAT数据库中学术发明家的匹配数据集及代码。完整的数据保存在zenodo ([10.5281/zenodo.10701432](https://zenodo.org/records/10702483)).


代码1：name_match_formal.ipynb
生成数据集1：Inventor_Scholar_Matching.csv
提供了发明人与学者的配对关系。
字段包括了专利数据库中的'psn_name', 'person_address', 'title_patstat_matching',论文数据库中的'author_name','affiliation_city', 'affiliation_country', 'affilname','doi_matching', 'title_scopus_matching',
标题的相似性'score_matching' ,以及发明人地址的相似性'invent_0_psn_name_similarity', 'invent_0_person_address_similarity',
       'person_address_similarity'。详细的数据流程可见论文。


代码2：describe_analysis.ipynb
生成数据集1：paper.csv
字段包括了论文数据库中的'author_idx','author_name','title', 'doi'

生成数据集2：patent.csv
字段包括了论文数据库中的'title', 'appln_kind', 'appln_auth', 'appln_nr_original', 'person_name'

生成数据集3：patent-paper-pair.csv
字段包括了专利-论文对的'title_patent', 'title_paper', 'appln_kind', 'appln_auth', 'appln_nr_original', 'person_name', 'doi', 'author_name'

代码3：predict_data.ipynb
提供了基础的描述性分析，以及包括卡方检验、回归分析在内的主要分析过程及结果。


This project provides matching datasets and code for academic inventors in the SCOPUS database and the PATSTAT database. Full data are availiable at zenodo ([10.5281/zenodo.10701432](https://zenodo.org/records/10702483)).

Code1: name_match_formal.ipynb
Generated Dataset 1: Inventor_Scholar_Matching.csv
This dataset provides the matching relationships between inventors and scholars.
The fields include 'psn_name', 'person_address', 'title_patstat_matching' from the patent database, and 'author_name', 'affiliation_city', 'affiliation_country', 'affilname', 'doi_matching', 'title_scopus_matching', title similarity score 'score_matching', as well as the similarity of inventor addresses 'invent_0_psn_name_similarity', 'invent_0_person_address_similarity', and 'person_address_similarity'.
Detailed data processing can be found in the paper.

Code2: describe_analysis.ipynb
Generated Dataset 1: paper.csv
This dataset includes fields from the paper database: 'author_idx', 'author_name', 'title', 'doi'.

Generated Dataset 2: patent.csv
This dataset includes fields from the paper database: 'title', 'appln_kind', 'appln_auth', 'appln_nr_original', 'person_name'.

Generated Dataset 3: patent-paper-pair.csv
This dataset includes fields for patent-paper pairs: 'title_patent', 'title_paper', 'appln_kind', 'appln_auth', 'appln_nr_original', 'person_name', 'doi', 'author_name'.

Code 3: predict_data.ipynb
This notebook provides basic descriptive analysis as well as the main analysis processes and results, including chi-square tests and regression analysis.
