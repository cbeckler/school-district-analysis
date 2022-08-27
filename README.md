# PyCitySchools with Pandas

## Overview of Project

### Purpose

The analyst had previously completed an analysis of academic results for the PyCity School District (found [here](https://github.com/cbeckler/school-district-analysis/blob/main/PyCitySchools.ipynb)), but the school board was concerned that the grades for reading and math for Thomas High School ninth graders may have been altered. The analyst was asked to repeat the previous analysis with the Thomas High School 9th grade scores removed, and compare to the previous results to assess the impact these scores may have had on the overall data.

The metrics by which the scores were assessed were: average math score, average reading score, percent of students passing math, percent of students passing reading, and the percent of students passing overall (which required passing both math *and* reading). These metrics were then also analyzed by school spending per capita, school size, and school type. Average scores (but not the percentages) were also assesed by grade level.

### Results

* The impact of dropping the Thomas High School 9th grade scores from the dataset was very small. The results from the analysis excluding them are:

![New Analysis District Results](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/new_district.png)

And the results from the prior analysis including them are:

![Old Analysis District Results](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/old_district.png)

Average math scores dropped by a tenth of a point, average reading scores were unchanged, and the percentages of passing in all categories dropped from one to three tenths of a percentage point. 

* The only row of data affected in the school summary is Thomas High School, and so those are the results the analyst will present here. The results from the analysis with 9th grade scores dropped are:

![New Analysis School Results](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/new_thomas.png)

And the results from the prior analysis including them are:

![Old Analysis School Results](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/old_thomas.png)

Though the results have been subtly changed by dropping the 9th grade scores, none of the metrics changed by more than three tenths of a point. This is indicative that the suspicious 9th grade scores were in fact in line with the other grade levels at Thomas High School.

* Unsurprisingly given that the averages and percentages for Thomas High School changed very little, it is still the second ranked school in the district based on overall passing percentage. The new results are:

![New Analysis Top Schools Results](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/new_top.png)

These are nearly identical to the prior top school results:

![Old Analysis Top Schools Results](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/old_top.png)

* The reason for the results changing very little can be seen when analyzing scores by grade. The scores by grade for Thomas High School can be seen below:

![Thomas High Math Scores By Grade](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/thomas_math.png)

![Thomas High Reading Scores By Grade](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/thomas_reading.png)

The average ninth grade scores for Thomas High School were all within one point of the scores for all other grade levels.

When taking the mean of ALL 9th grade scores in the district, exluding Thomas High School had a negligible effect. The mean reading math scores with Thomas was 80.4, without it 80.1. The mean reading score with Thomas was 82.5, without it 82.4.

* Due to how similar the results were for Thomas High School with its 9th grade scores removed to its initial results, removing the scores had zero impact on analysis by aggregate categories. The scores by school spending were identical for both analyses:

![Spending Analysis](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/spending.png)

* The results were likewise identical for scores by school size:

![Size Analysis](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/size.png)

* Finally, the results for scores by school type were also identical:

![Type Analysis](https://github.com/cbeckler/school-district-analysis/blob/main/Resources/type.png)


