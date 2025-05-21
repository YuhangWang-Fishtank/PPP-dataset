# PPP-dataset
Data and code release for PPP paper

本项目提供的SCOPUS数据库与PATSTAT数据库中学术发明家的匹配数据集及代码。论文见https://doi.org/10.1007/s11192-024-05207-9。完整的数据保存在zenodo (https://zenodo.org/records/15478277).
zenodo中的df_ppp.pickle是包含了发明人/作者的专利-论文匹配关系，因为存在发明人和作者的重复情况，总行数15,205,445和论文中的14,137,072并不一致。使用专利的appln_id和论文的eid去重后，数据集行数为14,137,072，这个去重后的数据集保存为df_ppp_drop_duplicates_appln_id_eid.pickle。
因为PATSTAT和Scopus都是非开放数据集，df_ppp.pickle和df_ppp_drop_duplicates_appln_id_eid.pickle都删去了两个数据库中的独有字段，包括PATSTAT的appln_id、person_id和Scopus的eid、author_id和afid。

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


The matching dataset and code for academic inventors in the SCOPUS database and PATSTAT database provided by this project. See paper(https://doi.org/10.1007/s11192-024-05207-9). The complete data is saved in Zenodo（https://zenodo.org/records/15478277).
The df_ppp.pickle in Zenodo includes a patent paper matching relationship between inventors/authors, but due to the duplication of inventors and authors, the total number of rows is 15205445, which is inconsistent with the 14137072 in the paper.
After using the patent's appln_id and the paper's eid for deduplication, the number of rows in the dataset is 14137072. This deduplicated dataset is saved as df_ppp-d rop-d uplicates_appd_id_id_ickle.
Because PATSTAT and Scopus are both non-open datasets, df_ppp. pickle and df_ppp_drop_duplicates_appd_id_id_eid.pickle have removed unique fields from both databases, including the "appln_id" and "person_id" of PATSTAT and the "eid", "author_id", and "afid" of Scopus.

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


==============================================update in 2024.9.30========================================================

新上传的数据集"Paper_Patent_Pair_v2.csv"包括了修订后的学术发明人（针对专利家族、跨国界学术发明人校对），具体代码将会在期刊审核后上传。

The newly uploaded dataset ("Paper_Patent_Pair_v2.csv") includes revised academic inventors (proofread for patent families and cross-border academic inventors), and the specific code will be uploaded after journal review.




