# code_understandability_data
Data concerning understandability of code snippets and static code measures

The following explanations make reference to two published papers:

[1] Muñoz Barón, M., Wyrich, M., & Wagner, S. (2020, October). An empirical validation of cognitive complexity as a measure of source code understandability. 14th ACM/IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM) (pp. 1-12).

[2] Lavazza, L., Abualkishik, A.Z., Liu, G., & Morasca, S. An Empirical Evaluation of the “Cognitive Complexity” Measure as a Predictor of Code Understandability. Journal of Systems and Software, to appear.

Understandability data were collected via experimental activities, which are reported in [1].

Each of the provided csv files concerns a specific aspect of readability, as specified in the file name. For instance, time_Data.csv concerns the time taken by participants in the empirical studies to understand code. The description of understandability aspects can be found in [1] and [2].

The provided csv files have all the same structure. Columns A to F were obtained from the supplemental material of [1], which is publicly available from https://doi.org/10.5281/zenodo.3949828.
Specifically,
column A "did" indicates the primary study from which Muñoz Barón et al. obtained the data.
column B "snippet_id" identifies the code snippet to which the data in the row refer.
column C "var_name" contains the did and the label of the understandability aspect considered in the row. Note that the label used is from the primary study, hence we may have different labels indicating the same concept, as well as the same label indicating slightly different concepts in different dids.
column E "value" provides the measure of the understandability aspect mentioned in column C.
column D "cognitive_complexity" provides the cognitive complexity measure of the code snippet identified by column B.
column F "pl" indicates the programming language used to code the snippet identified by column B.

Note that although each file groups data from different empirical studies, the data from a file are NOT homogeneous, since different studies measured different variants of the same understandability aspect, or the same aspect using different metrics. Therefore, only sets of data having the same values in column A and C are homogeneous and can be safely analyzed. 

Columns G to AN were obtained by applying the SourceMeter tool (https://www.sourcemeter.com/) to the code snippets identified by column B. Every column reports a different measure, whose name is in row 1.
Note that in some cases the value is NA, since SourceMeter does not provide a few metrics for some programming languages.
Not all the measures given in the csv files were used in [2]. The meaning of the measures used in [2] can be found in the paper, for the other measures, make reference to SourceMeter's documentation.

The provided data can be used for additional analysis, e.g., to apply model building techniques different from those used in [2], or to search for correlations involving different measures than those considered in [2].

The supplied data could also be used to study the correlation among code measures, without considering understandability. However, this kind of study has already been done, on a larger and more representative code base. See for instance
L. Lavazza, An Extended Study of the Correlation of Cognitive Complexity-related Code Measures
International Journal on Advances in Software, vol 15 no 1&2, 2022.
