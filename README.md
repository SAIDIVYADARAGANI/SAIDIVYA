**Tables created: **
 
create or replace table INTERVIEW_DB.PLAYGROUND_SAIDIVYA_DARAGANI.CASES_STATISTICS as (
    SELECT DISTINCTNew_Cases,New_Deaths,New_Recovered,New_Active_Cases,Total_Cases,Total_Deaths,Total_Recovered,Total_Active_Cases,Time_Zone,Total_Regencies,Total_Cities,Total_Districts,Total_Urban_Villages,Total_Rural_Villages,Population,New_Cases_per_Million,Total_Cases_per_Million,New_Deaths_per_Million,Total_Deaths_per_Million,Case_Fatality_Rate,Case_Recovered_Rate,Growth_Factor_of_New_Cases,Growth_Factor_of_New_Deaths
  )

create or replace table INTERVIEW_DB.PLAYGROUND_SAIDIVYA_DARAGANI.NEW_CASES_AND_DEATHS  as (
    SELECT DATE,New_Cases,New_Deaths,New_Cases_per_Million,New_Deaths_per_Million,Total_Cities    FROM CASES_STATISTICS
  )
  

create or replace table INTERVIEW_DB.PLAYGROUND_SAIDIVYA_DARAGANI.DEATH_STATISTICS as (
    SELECT DATE,New_Deaths,New_Deaths_per_Million,Total_Deaths_per_Million    FROM CASES_STATISTICS
  )

create or replace table INTERVIEW_DB.PLAYGROUND_SAIDIVYA_DARAGANI.NEW_CASES  as (
    SELECT DATE,New_Cases,New_Active_Cases,Total_Cases,,New_Cases_per_Million,Total_Cases_per_Million,Total_Cities    FROM CASES_STATISTICS
  )

create or replace table INTERVIEW_DB.PLAYGROUND_SAIDIVYA_DARAGANI.REPORT_MILLION as (
    SELECT DATE,New_Cases_per_Million,Total_Cases_per_Million,New_Deaths_per_Million,Total_Deaths_per_Million,Total_Cities    FROM CASES_STATISTICS
  )

**Views created:**

create or replace  view INTERVIEW_DB.PLAYGROUND_SAIDIVYA_DARAGANI.DEATHS_OVERVIEW  as (
    SELECT DATE, New_Deaths,Total_Deaths,New_Deaths_per_Million,Growth_Factor_of_New_Deaths
    FROM CASES_STATISTICS
  )


create or replace  view INTERVIEW_DB.PLAYGROUND_SAIDIVYA_DARAGANI.DAILY_STATS  as (
    SELECT DATE,New_cases,New_Deaths,New_Active_cases,New_Cases_per_Million,New_Deaths_per_Million,Growth_Factor_of_New_Deaths
    FROM CASES_STATISTICS
  )
 
