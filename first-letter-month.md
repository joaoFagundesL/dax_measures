```
MonthKey = 
YEAR('Extrato'[Data]) * 100 + MONTH('Extrato'[Data])
```

```
MonthInitial = 
UPPER( LEFT( FORMAT( 'Extrato'[Data].[Mês], "MMMM" ), 1 ) )
    & REPT( UNICHAR(8203), MONTH( 'Extrato'[Data]) )
```

Clicar em MonthInitial -> Ferramentas de Colunas -> Classificar por Coluna -> MonthKey
