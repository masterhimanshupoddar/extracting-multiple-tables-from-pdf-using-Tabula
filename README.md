# extracting-multiple-tables-from-pdf-using-Tabula
Extract multiple tables or particular table from a pdf file

extracting-tables-from-pdf-using-Tabula
extracting multiple tables from pdf using Tabula

#For extracting specific tables from a pdf we will be needing its coordinates.The steps to find coordinates is as follows- Use the Tabula app to grab table coordinates.

1.Open Tabula and upload your PDF into the web page that appears.<br/>
2.Select your table area(s) as usual and proceed to the "Preview & Export Extracted Data" step. <br/>
3.Under Export Format, select "Script" instead of CSV, and then click "Export" to download the generated code. Save this file. <br/>
4.Open the script you downloaded in a code editor. <br/>
5.The generated script contains measurements already filled in, based on what you selected in the Tabula app. <br/>
You can use this as a starting point to process many of the same type of document, <br/>
for example if you have a monthly report that is generated as separate PDFs for each month, <br/>
and the table you want is located in the exact same place each time.<br/>

eg of generated script "java -jar tabula-java.jar -a 234.019,38.991,313.638,555.396 -p 1 "$1" where "234.019,38.991,313.638,555.396" are the coordinates<br/>

the software tabula is also uploaded with the code.<br/>

#For extracting all the tables in a pdf file we can directly pass multiple_tables = True as an argument to the function<br/>
eg df = tabula.read_pdf(path, pages = '1', multiple_tables = True)<br/>
