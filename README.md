# Power-BI
# Problem Statement
The Excel file contains HR data of a company containing colums- name, gender, Designations before and after various financial years, people hired in FY 20, perforamnce rating, people leaving the company etc. We had find out the reason for gender ratio imbalance in Executive positions.

# Steps followed:
Step 1 : Load data into Power BI Desktop, dataset is a csv file
Step 2 : 2 pie charts were used- one to get a view of the gender ratio, another one to show the percent of people who were promoted
Step 3 : 2 multi row card were used- One for the average performance rating of the total workforce in FY 19 & FY 20, another to find the number of male & female candidates hired
        DAX query was used to find the number of male & female candidates hired
        Hire_men = CALCULATE(COUNTA('Pharma Group AG'[New hire FY20?]),'Pharma Group AG'[New hire FY20?]= "Y", 'Pharma Group AG'[Gender]="male")
        Hire_female = CALCULATE(COUNTA('Pharma Group AG'[New hire FY20?]),'Pharma Group AG'[New hire FY20?]= "Y", 'Pharma Group AG'[Gender]="female")
Step 4 : 1 card was used to show the percentage of people who gained promotion in FY21
        For Finding the percentage a DAX query was used:
        Promotion%_FY21 = DIVIDE(CALCULATE(COUNTA('Pharma Group AG'[Promotion in FY21?]),'Pharma Group AG'[Promotion in FY21?]="YES"),CALCULATE(COUNTA('Pharma Group AG'[Promotion in FY21?])))*100
                                                                            Pharma Group AG: Table name; Promotion in FY 21?: Column name
Step 5 : 4 stacked column chart were used: 1) To find number of people in different positions before FY20 promotion
                                            2) To find number of people in different positions after FY20 promotion
                                            3) To find number of people in different positions after FY21 promotion
                                            4) To find the gender variation among the people who left the company in FY20

# Insights/ Reasons
1) The hire ratio by gender is not at par with the gender ratio of present workforce
2) Even though the promotion percentage for male and female is same but the number of female employees in senior posts like Manager, Senior Manager, Director, Executive is very less than that of male employees

# Solutions
1) More number of female employees must be hired and promoted
2) The performance rating for male and female employees is almost the same so there will be no effect in the performance of the company if the gender balance is brought in
