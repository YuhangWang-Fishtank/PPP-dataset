# PPP-dataset
Data and code release for PPP paper

本项目提供的SCOPUS数据库与PATSTAT数据库中学术发明家的匹配数据集及代码。论文Trace on both sides: a two-step text mining method to identify academic inventors’ patent–paper pairs见(https://doi.org/10.1007/s11192-024-05207-9).
完整的数据保存在zenodo (https://zenodo.org/records/15478277).
zenodo中的df_ppp.pickle是包含了发明人/作者的专利-论文匹配关系，因为存在发明人和作者的重复情况，总行数15,205,445和论文中的14,137,072并不一致。使用专利的appln_id和论文的eid去重后，数据集行数为14,137,072，这个去重后的数据集保存为df_ppp_drop_duplicates_appln_id_eid.pickle。同样，论文中的学者数量是使用author_id统计，发明人数量是使用person_id统计，这两个字段也因为权限问题被删除，因此数据集中的直观数量可能与论文汇报的数目有出入。
因为PATSTAT和Scopus都是非开放数据集，df_ppp.pickle和df_ppp_drop_duplicates_appln_id_eid.pickle都删去了两个数据库中的独有字段，包括PATSTAT的appln_id、person_id和Scopus的eid、author_id和afid。

代码1：name_match_formal.ipynb
提供了发明人与学者的配对关系。


代码2：describe_analysis.ipynb
提供了基础的描述性分析，以及包括卡方检验、回归分析在内的主要分析过程及结果。


The matching dataset and code for academic inventors in the SCOPUS database and PATSTAT database provided by this project. See paper "Trace on both sides: a two-step text mining method to identify academic inventors’ patent–paper pairs" (https://doi.org/10.1007/s11192-024-05207-9). The complete data is saved in Zenodo（https://zenodo.org/records/15478277).
The df_ppp.pickle in Zenodo includes a patent paper matching relationship between inventors/authors, but due to the duplication of inventors and authors, the total number of rows is 15205445, which is inconsistent with the 14137072 in the paper.
After using the patent's appln_id and the paper's eid for deduplication, the number of rows in the dataset is 14137072. This deduplicated dataset is saved as df_ppp-d rop-d uplicates_appd_id_id_ickle. Similarly, the number of scholars in the paper is calculated using author_id, and the number of inventors is calculated using person_id. These two fields have also been removed due to permission issues, so the intuitive quantity in the dataset may differ from the number reported in the paper.
Because PATSTAT and Scopus are both non-open datasets, df_ppp. pickle and df_ppp_drop_duplicates_appd_id_id_eid.pickle have removed unique fields from both databases, including the "appln_id" and "person_id" of PATSTAT and the "eid", "author_id", and "afid" of Scopus.

Code1: name_match_formal.ipynb
This dataset provides the matching relationships between inventors and scholars.

Code2: describe_analysis.ipynb
This notebook provides basic descriptive analysis as well as the main analysis processes and results, including chi-square tests and regression analysis.



