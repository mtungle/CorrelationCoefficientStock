
# Correlation coefficient of Autralian stocks
Text.

## The data set

```
AAC,20090102,1.945,1.97,1.875,1.875,140313
AAH,20090102,0.835,0.85,0.835,0.85,61427
AAM,20090102,0.085,0.1,0.085,0.1,155777
AAO,20090102,0.022,0.022,0.022,0.022,7000
AAQ,20090102,0.16,0.16,0.16,0.16,1600
AAR,20090102,0.024,0.025,0.023,0.023,292683
AAU,20090102,0.31,0.31,0.31,0.31,15000
AAX,20090102,2.23,2.35,2.16,2.2,249114
ABB,20090102,7.55,7.55,7.12,7.23,65722
ABC,20090102,2.09,2.09,2.02,2.05,147418
ABJ,20090102,0.017,0.019,0.017,0.019,185000
ABP,20090102,0.215,0.235,0.19,0.205,3461719
ABU,20090102,0.016,0.016,0.015,0.015,500000
ABY,20090102,0.15,0.19,0.15,0.175,2800449
```

## Data preperation

```R
df <- read.table("all.txt", header = FALSE,sep = ",")
company_codes<-unique(df$V1)
dates<-unique(df$V2)
string_company_codes=strsplit(toString(company_codes),", ")
string_dates=strsplit(toString(dates),", ")
price_matrix<-matrix(data=NA,nrow=lengths(string_company_codes),ncol=lengths(string_dates))
rownames(price_matrix)<-unlist(string_company_codes)
colnames(price_matrix)<-unlist(string_dates)
```

## Correlation coefficient of stocks on the same business day

## Correlation coefficient of stocks on 1-day difference



