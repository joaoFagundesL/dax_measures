```
CF Max Min Saldo = 
VAR max_val = MAXX(ALLSELECTED(Extrato[ReportingPeriod]), [Total Saldo])
VAR min_val = MINX(ALLSELECTED(Extrato[ReportingPeriod]), [Total Saldo])
RETURN
SWITCH(
    TRUE(),
    [Total Saldo] = max_val, "Green",
    [Total Saldo] = min_val, "Red",
    BLANK() 
)
```

Change to bar chart -> conditional formatting -> set the measure -> back line chart
