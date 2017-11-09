## **Analysis of Largest Dog Breed Dataset** 

### Introduction

The Largest Dog Breed Dataset *(Ref. 1)* consists of 10 different .csv files that were merged into one; one for each of the years 2007 through 2016.  The same seven columns appear in each file; LicenseType, Breed, Color, DogName, OwnerZip, ExpYear, ValidDate.  The average number of rows per file is about 30,000.    

### Dataset Origin and Significance

The origination of the data set is a Pennsylvania State Law that mandates all dogs 3 months of age or older must be licensed. Dog 
Licenses must be purchased by January 1st of each year regardless of when the license was purchased the previous year.  An annual 
license is $8.50 and a lifetime license is $51.50. Discounts are available to older adults and people with disabilities *(Ref. 2)*; 
hence the appearance of these types of listings in the LicenseType column. 

The license fee funds the Pennsylvania Department of Agriculture Bureau of Dog Law Enforcement.  State Dog Wardens perform "License and 
Rabies Compliance Checks" throughout the Commonwealth using PADogLicense.com Real Time system to track unlicensed dogs. State Dog 
Wardens may issue fines up to $300.00 plus court cost per dog for violation of this law.  One of the benefits of licensing is dog owners
can use a free website *(Ref. 3)* to possibly be reunited with their lost pet. More than 5,695 lost pets have been reunited with their 
owners and over 540 pets are still missing (time range for these data was not provided in the literature).   

### Dataset Overview

The data set changes very little year over year due to the same pet being registered every year of the life span.  This statement 
was validated by comparing a few of the single year data sets to each other and to the aggregate.  The 10 .csv files were merged more for the learning exercise than to enrich the data set and improve accuracy.

A count of blank fields is summarized in the Jupyter notebook.  The actual 2016 data file was scanned for other missing data:  
1. Breed is populated as "." for 0.1% of the entries and "other" for 0.2% of the entries
2. Name is populated as "?" or some version of "Not given" for 0.1% of the entries
3. Color is populates as "." or "Other" in 1% of the entries

The flaws described above were deemed insignificant for this exercise and were not treated.

As of November 2016, the American Kennel Club (AKC) recognizes 202 different breeds of dogs; however, the data set shows 344 unique
breeds.  That is because there are many listings for "mixed" (re: Figure 1), for "designer" dogs like Labradoodles (cross between Labrador Retriever 
and Poodle = temperment of Lab but don't shed), and some for breeds that are not recognized by the AKC.  Additionally, there 
appears to be a lack of standard nomenclature.  For example, some abbreviations resulted in duplicates, and "puppy" and "tag" appear 
but only twice in the 2016 dataset.  

Figure 1:  Breed Counts, 2007-2016

![alt text](https://github.com/Jminic81/Dogs7/blob/master/dogbar.png)

Trending for the top five most popular breeds is shown in Figure 2.

Figure 2:  Top Five Breeds, Counts vs. Year

![alt text](https://github.com/Jminic81/Dogs7/blob/master/dogline.png)

Frequency for Color and DogName were measured but as expected, color was predominantly black, brown, white or mixes thereof, and DogName was varied and in many cases amusing. 

160 different zip codes in Pennsylvania are represented.  This is a fraction of the total 2,174 zip codes in PA for 67 counties.  Re:  below - looking at the top zip codes by count, all of the locations are within a 15 mile radius of Pittsburgh.  It is conceivable that there are about 30,000 dogs just in the greater Pittsburgh area as there are millions of licenced dogs in the state of Pennsylvania.

|__ZipCode__|__Count__|__City__         | 
|:---------:|--------:|:----------------|
| 15235     | 11443   |  Pittsburgh     |
| 15108     | 11302   |  Coraopolis     |
| 15044     |  9145   |  Gibsonia       |
| 15102     |  9144   |  Bethel Park    |
| 15236     |  8519   |  Pittsburgh     |
| 15146     |  8351   |  Monroeville    |
| 15136     |  7655   |  Mc Kees Rocks  |
| 15239     |  7546   |  Pittsburgh     |
| 15101     |  7223   |  Allison Park   |

### Analysis

The Jupyter notebook "Dogs Merge" in ths repository contains the raw data analysis and visualizations.
 
### References:
1.  https://www.kaggle.com/kingburrito666/data-analysis-with-dog-breeds/data.  Dataset and kernel by Liam Larsen.
2.  http://padoglicense.com/
3.  www.palostpet.com
