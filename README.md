# Census-Project

This analyses the census of a moderately sized town to make recommendations for 
investment in future services and use cases for developments on an unused plot of land. To make 
these recommendations, the census data has firstly been cleaned to correct data errors and missing 
records, which is detailed in the first section of this report.
Subsequent sections of the report will highlight key analyses undertaken specifically aimed at to 
support recommendations provided. This includes, initially, an overview of the town’s population 
demographics, followed by detailed analysis of the town’s predicted population growth, 
employment trends, commuters, and occupancy rates. 

# Data Cleaning
Census data was cleaned to correct the data errors; a full logbook of all cleaning undertaken can be 
found in the corresponding Jupyter Notebook.
Blank data were imputed by inferring information from an individual’s record or others in their 
household (in the case of missing surnames). Records that could not be imputed with referential 
information were imputed to ‘None’ or ‘Unknown’ (in the case of Occupation).
Four religions were converted to ‘None’ - Sith, Undecided, Housekeeper and Ironer. Sith was 
determined to be a deliberately misleading input due to only four entries and this has been known 
to be written as a ‘joke’ entry in previous censuses (BBC, 2016). Housekeeper and Ironer were 
deemed to be individual errors.
Religion for minors (under 18) were primarily NaN entries, aside from 7 which were a mixture of 
None or Triangulism. Given NaN was the most frequent value for under 18s, all those with an entry 
in this variable under 18 where converted to NaN. The impact of this is it will not be possibly to 
analyse religious transmission from parent to children – though this would have been difficult 
regardless, given most children had NaN as a religion.
Similarly, individuals under the age of 18 have NaN as a marital status. An exception has been made 
for those 16 or above, as it is legal to marry with parental consent (Marriage Act, 1949:s3). A further 
exception has been made for those under 18 who do not live with another over 18 in the household, 
whose records have not been imputed as it is possible to move out of a family home before 18
(NSPCC, 2020).
One household was removed from the dataset. In this household, a child of 15 was married with a 
child, listed as Head of the household, and had a husband over 18. As there are two major
inconsistencies or a potentially illegal relationship, this household was dropped from the dataset; it 
was not deemed significant (three records) to the overall analysis enough to impute multiple counts 
of incorrect data across a household.
Outliers were removed for one record of an age at 111 (imputed to match the spouse’s age) and four 
individuals widowed at age 18 or below, as detailed in the boxplot distribution:
Although there are several outliers above, it is not unusual people to become widowed at old age as 
much as it for someone to become widowed at 18. Therefore, these records were considered too 
unlikely to be correct and imputed to ‘Single’ (if 18) or NaN (if under 18).
Records which listed Occupation as ‘Unemployed’ for individuals over 65 were imputed to ‘Retired, 
unemployed’. Although it is possible to be unemployment upon reaching retirement age, these 
should not be considered in future analyses of unemployment as those over 65 would not usually be 
eligible for work (Gov.uk).

# Recommendations
Given the large number of lodgers emigrating to the town, and the high number of commuters, 
there is both a need to build a train station and potentially invest in low-density housing. However, a 
train station may not benefit families who are renting rooms to lodgers. In this case, low-density 
housing would benefit lodgers moving to the town, families, those who are divorced with young 
children who may need to downsize.
It is likely in future years those smaller houses occupied by retired individuals will eventually become 
available. At this point, there is more opportunity for the town population to grow and develop, 
inviting more immigration from those looking for work and further relieve the housing shortage. In 
the future, then, a train station may be worth investing in, but at this point low density housing will 
benefit more of the population.
Given the high ages of some individuals, and the relatively good income of most in the town, it is 
likely they will live longer. Very few suffered from an infirmity, however this may not be the case as 
the population ages. Thus, investing in age old care should be a priority above other services. 
Other services to invest in, such as schooling or the general infrastructure, is not warranted at 
present due to the population’s relatively small growth year on year. However, the aging population 
will only increase and require more care, so it is pertinent to invest in this before that happens.
Bibliography
