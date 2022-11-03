# SharkAttack
Project Name

## Active
Project status(Active, On-Hold, Completed)

## Project objective
To practice tools and procedures learned during data cleaning and manipulation classes in Ironhack bootcamp. 

### Paragraph with introduction/ objective of project

Sharks are one of the most feared creatures in the world. The goal of this dataset is to inform people about the risks associated with coastal water activities and to improve shark/human relations by educating people on factors that contribute to shark attacks. The analysis looked, specially, into the relationship between the number of events and the moon phases, the seasons of the year and the land-ocean temperature.

### Methods
First cleaning
Raise a question
More cleaning and preparing data to answer the question 
Raise a second question
More cleaning and preparing data to answer the second question 
(...)

### List with methods, ex:

Function declaration
Manipulation (drop, replace, merge)
Grouping
Visualization (next step) 

### List with used technologies, ex:

Python
Pandas


### Paragraph with a description of the dataset, sources, characteristics ,etc.
It was used 3 datasets, all of them found on Kaggle:
Shark Attack - A table of shark attack incidents compiled by the Global Shark Attack File.
Moon Calendar - The full moon is the lunar phase when the Moon appears fully illuminated from Earth's perspective. There are exactly 1,867 full moons between 1900 and 2050. 
(next step) Land-Ocean - The change in global surface temperature relative to 1951-1980 average temperatures in data from Nasa. 



### Steps

#quantos ataques aconteceram por ano
2015    141
2017    137
2016    129
2011    128
2014    123
2013    122
2009    119
2008    117
2012    115
2007    108
2005    103
2010    100
2006     99
2000     90
2001     89
2004     89
2002     87
2003     85
1959     78
1962     75
Name: year2, dtype: int64

#em qual mês aconteceu mais ataques
shark['month'].value_counts()
7     623
8     553
9     524
1     499
6     473
4     426
12    422
10    414
3     383
11    379
5     367
2     359



#intervalo de tempo entre um ataque e outro
median-5
np.median(np.diff(shark['date_clean']))
x = np.timedelta64(432000000000000, 'ns')
days = x.astype('timedelta64[D]')
days / np.timedelta64(1, 'D')

mean - 18
x = np.timedelta64(1567679187181249, 'ns')
days = x.astype('timedelta64[D]')
days / np.timedelta64(1, 'D')

max - 36515


#em quantos dias houve ataques - 4752
len(shark['date_clean'].unique())

#numero de dias com mais de um ataque
sum(shark.groupby('date_clean').count()['case_number']!=1)
575

#primeira ideia era verificar se havia variação entre estações do ano e número de ataques
#dificuldade diferentes estações de acordo com o hemisfério sul e norte
#lua e influencia nas mares (muda o visual, mas a fase é a mesma em todo planeta)



#tubarão é o lobisomen dos mares? 

crescente    1296
minguante    1249
nova         1240
cheia        1179


### Add here any insights you had during the project

month sazonality (seasons) australia e eua
number of cases increased through the years - ocean_temperature (next question)




### Conclusion

This phenomenon varied over time 

## Final conclusion

It seems to us that there is a  between case numbers and time variables

### Contact

linkedin, github, gmail
