&nbsp;                                                **CREATE DAX FORMULA**







* -- **CREATE CUSTOM CALLANDER IN DAX FORMULA**



* -- SYNTAX : - LIST.DATES(START AS DATE,COUNT AS NUMBER, STEP AS DURATION)



*  **LIST.DATES(#DATE(2013,1,1),365,#DURATION(1,0,0,0)**





* -- **MONTH TO DATE - QUATER TO DATE - YEAR TO DATE**



* MTD = TOTALMTD(\[Total\_Sales],Custom\_Callendar\[Date].\[Date]) 



* -- **SAME PERIOD LAST YEAR**



* Same Period last year = CALCULATE(\[Total\_Sales],SAMEPERIODLASTYEAR(Custom\_Callendar\[Date].\[Date]))



* -- **TOTAL QUANTITY** 



* Total\_Quantity = SUM(Sales\_Data\[Units Sold]) 



* -- **TOTAL SALES SOLD BY UNIT \& PRICE UNIT**



* Total\_Sales = SUMX(Sales\_Data,Sales\_Data\[Units Sold]\*Sales\_Data\[Price Per Unit])



* -- **TOTAL TRANSACTION** 



* Transaction = COUNTROWS(Sales\_Data) 



* -- **AVERAGE PRICE**



* Average\_Price = AVERAGE(Sales\_Data\[Price Per Unit]) 
