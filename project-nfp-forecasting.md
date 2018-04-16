# NFP Forecasting
Sam Choi, Eric Xu  
<!-- Don't edit in between this line and the one below -->

*Source file* 
<a href='data:text/x-markdown;base64,LS0tCnRpdGxlOiAiTkZQIEZvcmVjYXN0aW5nIgphdXRob3I6ICJTYW0gQ2hvaSwgRXJpYyBYdSIKb3V0cHV0OgogIGh0bWxfZG9jdW1lbnQ6CiAgICBmaWdfaGVpZ2h0OiAzCiAgICBmaWdfd2lkdGg6IDUKICAgIGtlZXBfbWQ6IHRydWUKICBwZGZfZG9jdW1lbnQ6IGRlZmF1bHQKICB3b3JkX2RvY3VtZW50OiBkZWZhdWx0Ci0tLQo8IS0tIERvbid0IGVkaXQgaW4gYmV0d2VlbiB0aGlzIGxpbmUgYW5kIHRoZSBvbmUgYmVsb3cgLS0+CmBgYHtyIGluY2x1ZGU9RkFMU0V9CmxpYnJhcnkoRGF0YUNvbXB1dGluZykKbGlicmFyeShhc3RzYSkKYGBgCipTb3VyY2UgZmlsZSogCmBgYHtyLCByZXN1bHRzPSdhc2lzJywgZWNobz1GQUxTRX0KaW5jbHVkZVNvdXJjZURvY3VtZW50cygpCmBgYAojIyMjIE9iamVjdGl2ZQpVc2luZyBkYXRhIGZyb20gSmFudWFyeSAyMDEwIHRvIE1hcmNoIDIwMTcsIHdlIGFpbSB0byBmb3JlY2FzdCBOb25mYXJtIHBheXJvbGxzIGZvciB0aGUgZm9sbG93aW5nIHllYXIgKEFwcmlsIDIwMTcgdG8gTWFyY2ggMjAxOCkuCjxicj4KCiMjIyMgU0EgKFBBWUVNUykgYW5kIE5TQSAoUEFZTlNBKSBORlAgRGF0YQpgYGB7cn0KUEFZRU1TIDwtIHJlYWQuY3N2KGZpbGUgPSAiUEFZRU1TLmNzdiIsIGhlYWRlciA9IFRSVUUsIHNlcCA9ICIsIikKUEFZTlNBIDwtIHJlYWQuY3N2KGZpbGUgPSAiUEFZTlNBLmNzdiIsIGhlYWRlciA9IFRSVUUsIHNlcCA9ICIsIikKbmZwX3NhX3RzIDwtIHRzKFBBWUVNU1syXSkKbmZwX25zYV90cyA8LSB0cyhQQVlOU0FbMl0pCmBgYAoKIyMjIyBTcGxpdHRpbmcgdGhlIGRhdGFzZXQKVHJhaW5pbmc6IEphbnVhcnkgMjAxMCAtIE1hcmNoIDIwMTcKVGVzdGluZzogQXByaWwgMjAxNyAtIE1hcmNoIDIwMTgKYGBge3J9Cm5mcF9zYV90cmFpbmluZ190cyA8LSB0cyhQQVlFTVNbODUzOjkzOSxdWzJdKQpuZnBfc2FfdGVzdGluZ190cyA8LSB0cyhQQVlFTVNbOTQwOjk1MSxdWzJdKQpuZnBfbnNhX3RyYWluaW5nX3RzIDwtIHRzKFBBWU5TQVs4NTM6OTM5LF1bMl0pCm5mcF9uc2FfdGVzdGluZ190cyA8LSB0cyhQQVlOU0FbOTQwOjk1MSxdWzJdKQpgYGAKCiMjIyMgCgoKCgoKCgoKCgoK' target='_blank' title='User  at /Users/samchoi' download='project-nfp-forecasting.Rmd'> &#8658; project-nfp-forecasting.Rmd</a>  
#### Objective
Using data from January 2010 to March 2017, we aim to forecast Nonfarm payrolls for the following year (April 2017 to March 2018).
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











