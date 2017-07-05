

Introduction: This is the introduction.
This the next line.


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




    [1] 2




```R

```

