# Project NFP - Forecasting
Sam Choi, Eric Xu  
<!-- Don't edit in between this line and the one below -->

*Source file* 
<a href='data:text/x-markdown;base64,LS0tCnRpdGxlOiAiUHJvamVjdCBORlAgLSBGb3JlY2FzdGluZyIKYXV0aG9yOiAiU2FtIENob2ksIEVyaWMgWHUiCm91dHB1dDoKICBodG1sX2RvY3VtZW50OgogICAgZmlnX2hlaWdodDogMwogICAgZmlnX3dpZHRoOiA1CiAgICBrZWVwX21kOiB0cnVlCiAgcGRmX2RvY3VtZW50OiBkZWZhdWx0CiAgd29yZF9kb2N1bWVudDogZGVmYXVsdAotLS0KPCEtLSBEb24ndCBlZGl0IGluIGJldHdlZW4gdGhpcyBsaW5lIGFuZCB0aGUgb25lIGJlbG93IC0tPgpgYGB7ciBpbmNsdWRlPUZBTFNFfQpsaWJyYXJ5KERhdGFDb21wdXRpbmcpCmxpYnJhcnkoYXN0c2EpCmBgYAoqU291cmNlIGZpbGUqIApgYGB7ciwgcmVzdWx0cz0nYXNpcycsIGVjaG89RkFMU0V9CmluY2x1ZGVTb3VyY2VEb2N1bWVudHMoKQpgYGAKCiMjIyMgT2JqZWN0aXZlClVzaW5nIGRhdGEgZnJvbSBKYW51YXJ5IDIwMTAgdG8gTWFyY2ggMjAxNywgd2UgYWltIHRvIGZvcmVjYXN0IE5vbmZhcm0gcGF5cm9sbHMgZm9yIHRoZSBmb2xsb3dpbmcgMTIgbW9udGhzIChBcHJpbCAyMDE3IHRvIE1hcmNoIDIwMTgpLiAgCjxicj4KCiMjIyMgU0EgKFBBWUVNUykgYW5kIE5TQSAoUEFZTlNBKSBORlAgRGF0YQpgYGB7cn0KUEFZRU1TIDwtIHJlYWQuY3N2KGZpbGUgPSAiUEFZRU1TLmNzdiIsIGhlYWRlciA9IFRSVUUsIHNlcCA9ICIsIikKUEFZTlNBIDwtIHJlYWQuY3N2KGZpbGUgPSAiUEFZTlNBLmNzdiIsIGhlYWRlciA9IFRSVUUsIHNlcCA9ICIsIikKbmZwX3NhX3RzIDwtIHRzKFBBWUVNU1syXSkKbmZwX25zYV90cyA8LSB0cyhQQVlOU0FbMl0pCmBgYAoKIyMjIyBTcGxpdHRpbmcgdGhlIGRhdGFzZXQKVHJhaW5pbmc6IEphbnVhcnkgMjAxMCAtIE1hcmNoIDIwMTcgIApUZXN0aW5nOiBBcHJpbCAyMDE3IC0gTWFyY2ggMjAxOCAgCmBgYHtyfQpuZnBfc2FfdHJhaW5pbmdfdHMgPC0gdHMoUEFZRU1TWzg1Mzo5MzksXVsyXSkKbmZwX3NhX3Rlc3RpbmdfdHMgPC0gdHMoUEFZRU1TWzk0MDo5NTEsXVsyXSkKbmZwX25zYV90cmFpbmluZ190cyA8LSB0cyhQQVlOU0FbODUzOjkzOSxdWzJdKQpuZnBfbnNhX3Rlc3RpbmdfdHMgPC0gdHMoUEFZTlNBWzk0MDo5NTEsXVsyXSkKYGBgCgojIyMjIAoKCgoKCgoKCgoKCg==' target='_blank' title='User  at /Users/samchoi' download='project-nfp-forecasting.Rmd'> &#8658; project-nfp-forecasting.Rmd</a>  

#### Objective
Using data from January 2010 to March 2017, we aim to forecast Nonfarm payrolls for the following 12 months (April 2017 to March 2018).  
<br>

#### SA (PAYEMS) and NSA (PAYNSA) NFP Data

```r
PAYEMS <- read.csv(file = "PAYEMS.csv", header = TRUE, sep = ",")
PAYNSA <- read.csv(file = "PAYNSA.csv", header = TRUE, sep = ",")
nfp_sa_ts <- ts(PAYEMS[2])
nfp_nsa_ts <- ts(PAYNSA[2])
```

#### Splitting the dataset
Training: January 2010 - March 2017  
Testing: April 2017 - March 2018  

```r
nfp_sa_training_ts <- ts(PAYEMS[853:939,][2])
nfp_sa_testing_ts <- ts(PAYEMS[940:951,][2])
nfp_nsa_training_ts <- ts(PAYNSA[853:939,][2])
nfp_nsa_testing_ts <- ts(PAYNSA[940:951,][2])
```

#### 











