# Data-Cleaning_Excel

The dataset comprises the supplier's invoice statement for motorcycle sales, which contains irregular numbers, inappropriate date formats, excessive spaces, and incorrect amount formats. 
Functions such as TRIM, CLEAN, CONCAT, TEXTJOIN, LEFT, RIGHT, MID, VALUE, and SUBSTITUTE were utilized to clean the data.

Task: Clean the dataset with Microsoft Excel and complete the table

The raw data is from column A to column J, while the cleaned data is from column K to Q

Column K:
Concatenate columns A and B using the ampersand symbol
=A2&"-"&B2

Column L:
Join text from H2:J2, using “-” as the delimiter using the TEXTJOIN function
=TEXTJOIN("-",TRUE,H2:J2)

Column M:
Extract the invoice month from column D using the LEFT function
=LEFT(D2,3)

Column N:
Extract the purchase order number from column G using the RIGHT function
=RIGHT(G2,6)

Column O:
Extract the location from column G using the MID function
=MID(G2,4,LEN(G2)-10)

Column P:
Remove strange characters and extra spaces from column E, using the TRIM and CLEAN function
=UPPER(TRIM(CLEAN(E2)))

Column Q:
Substitute “S” in the amount to “$”, remove the extra space in between them and convert it to a number using SUBSTITUTE and VALUE function
=VALUE(SUBSTITUTE(SUBSTITUTE(F2,"S","$"),MID(F2,2,1),""))


