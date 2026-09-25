# DAX Measures

This document contains the DAX measures used for the Marketing Power BI Dashboard.

---


```DAX
Total Leads = SUM(Course_Data[Leads])

Total Converted = SUM(Course_Data[Converted])

Total Revenue = SUM(Course_Data[Revenue])

Conversion Rate = DIVIDE([Total Converted],[Total Leads],0)

Source Conversion Rate = 
DIVIDE(
    SUM(Platforms_Data[Converted]),
    SUM(Platforms_Data[Leads]),
    0
)

Profit % = 
DIVIDE(
    [Total Payment],
    [Total Amount],
    0
)
