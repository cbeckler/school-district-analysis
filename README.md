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

## Summary

Though small, there are four changes to the results that may be highlighted:

1) The most important would be a minor drop in the overall passing rate for the district, which fell 0.3% from 65.2 to 64.9. As before, the numbers of students with passing scores in both math and reading were divided by the total number of students--and for the new analysis, the Thomas High 9th graders were excluded from the total count to ensure consistency, since their scores were dropped. Though minor, the overall passing rate for the district had been raised slighty by the potentially fradulent scores.
2) Again looking at the district analysis, it looks like within the overall passing rate, the math scores were affected slightly more than the reading scores. The math passing rate dropped 0.2% from 75.0 to 74.8, while the reading passing rate dropped 0.1%, from 85.8 to 85.7.
3) For Thomas High School itself, the overall passing rate dropped 0.3%, from 90.9 to 90.6. As with the overall average, the Thomas High 9th graders were excluded from the student body count for calculations. The 0.3% drop mirrors the results in the district level data.
4) However, interestingly, in contrast to the district results, in Thomas High the reading passing rates were more affected by dropping the 9th grade scores than the math passing rates. The reading passing rate dropped 0.3% from 97.3 to 97.0, while the math passing rate dropped 0.1% from 93.3 to 93.2. This suggests that Thomas High School may carry more impact on district math scores than it does on reading, since if the impact of the different types of scores was 1:1 with the district, you would expect math rates to drop more steeply than reading in both, rather than in the district only.

The full analysis of the school district scores with the Thomas High 9th grade scores dropped may be found [here](https://github.com/cbeckler/school-district-analysis/blob/main/PyCitySchools_Challenge.ipynb).
