# 5_1-Total-Number-of-EVs-by-Make-over-Time-in-the-UK
Line graph of Total Number of EVs by Make over Time in the UK

Procedure for Collecting Electric Vehicle Statistics Data in the United Kingdom:
      1.	Access the official website of the UK Government's statistics, https://www.gov.uk/government/collections/vehicles-statistics.
      2.	Navigate to the section dedicated to vehicle statistics and proceed to open the page dedicated to vehicle statistics.
      3.	Locate and access the most recent report on vehicle licensing statistics.
      4.	Within the designated page for Vehicle Licensing Statistics for the specified year, proceed to the documents section and initiate the download of the latest tables in zip file format.
      5.	From the downloaded files, identify and extract the relevant data from the "VEH0171.ods" file, focusing solely on the required information related to electric vehicles.

Procedure for Cleaning the "VEH0171.ods" File:
      1.	Open the "VEH0171.ods" file and navigate to the sheet named "VEH0171b_GenModels."
      2.	Copy all columns containing Electric Vehicle (EV) data, along with their respective column headers, to a new workbook.
      3.	Remove the columns labelled "Geography" and "Units" since their values are identical throughout.
      4.	Rename the column headers as follows:
            a.	Change "BodyType [note 2]" to "BODYTYPE"
            b.	Change "Make [note 6]" to "MAKE"
            c.	Change "Generic model [note 6]" to "MODEL"
      5.	Eliminate all rows that contain the model data "MISSING" by using the RIGHT and IF functions along with the Filter.
      6.	Convert the quarterly data into yearly data by calculating the sum of each quarter and label the header as "YEAR" in YYYY format.
      7.	Calculate the overall row total for each model and name the corresponding header as "TOTAL."
      8.	Delete all the quarterly data, as it is no longer necessary.
      9.	Verify and convert all text data into uppercase for consistency.
      10.	Save the cleaned file as "SOURCE_DATA" in Excel workbook format.

5_1 Procedure to arrive at the data to create multiple line chart of “Total Number of EVs by Make over Time in the UK”.
      1.	Open the SOURCE_CODE excel file and insert a pivot table.
      2.	Add “MAKE” in rows and all the years in values.
      3.	Filter the make for only top 10 as found in 1_3 procedure.
      4.	Now copy and paste the table to a new workbook where headers are years, and first column is manufacturer.
      5.	Save the file as CSV format with name as “5_1.CSV”.
 
