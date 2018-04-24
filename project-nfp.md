# Project NFP - EDA
Sam Choi, Eric Xu  
<!-- Don't edit in between this line and the one below -->

*Source file* 
<a href='data:text/x-markdown;base64,LS0tCnRpdGxlOiAiUHJvamVjdCBORlAgLSBFREEiCmF1dGhvcjogIlNhbSBDaG9pLCBFcmljIFh1IgpvdXRwdXQ6CiAgaHRtbF9kb2N1bWVudDoKICAgIGZpZ19oZWlnaHQ6IDMKICAgIGZpZ193aWR0aDogNQogICAga2VlcF9tZDogdHJ1ZQogIHBkZl9kb2N1bWVudDogZGVmYXVsdAogIHdvcmRfZG9jdW1lbnQ6IGRlZmF1bHQKLS0tCjwhLS0gRG9uJ3QgZWRpdCBpbiBiZXR3ZWVuIHRoaXMgbGluZSBhbmQgdGhlIG9uZSBiZWxvdyAtLT4KYGBge3IgaW5jbHVkZT1GQUxTRX0KbGlicmFyeShEYXRhQ29tcHV0aW5nKQpsaWJyYXJ5KGFzdHNhKQpgYGAKKlNvdXJjZSBmaWxlKiAKYGBge3IsIHJlc3VsdHM9J2FzaXMnLCBlY2hvPUZBTFNFfQppbmNsdWRlU291cmNlRG9jdW1lbnRzKCkKYGBgCgojIyMgTkZQIEVEQQpXZSBhaW0gdG8gZXhwbG9yZSB0d28gdmVyc2lvbnMgb2YgTkZQIGRhdGE6IFBBWUVNUyBhbmQgUEFZTlNBLiBQQVlFTVMgaXMgYSBkYXRhc2V0IHdpdGggc2Vhc29uYWxseSBhZGp1c3RlZCB2YWx1ZXMsIGFuZCBQQVlOU0EgaXMgYSBkYXRhc2V0IHdpdGhvdXQgc2Vhc29uYWwgYWRqdXN0bWVudHMuIFRoZSBkYXRhIGlzIHJlY29yZGVkIGluIHRob3VzYW5kcyBvZiBwZXJzb25zIChqb2JzIGNyZWF0ZWQpLiBUaGUgZGF0YXNldHMgY29udGFpbiBtb250aGx5IE5GUCByZXBvcnQgdmFsdWVzIGZyb20gSmFudWFyeSAxOTM5IHRvIE1hcmNoIDIwMTguICAKPGJyPgoKCiMjIyMgU2Vhc29uYWxseSBBZGp1c3RlZCAoUEFZRU1TKQpgYGB7ciBvdXQud2lkdGggPSAiNzAlIiwgZHBpID0gNDAwfQpQQVlFTVMgPC0gcmVhZC5jc3YoZmlsZSA9ICJQQVlFTVMuY3N2IiwgaGVhZGVyID0gVFJVRSwgc2VwID0gIiwiKQpuZnBfc2FfdHMgPC0gdHMoUEFZRU1TWzJdKQpwbG90LnRzKG5mcF9zYV90cywgbWFpbiA9ICJTZWFzb25hbGx5IEFkanVzdGVkIFRvdGFsIE5vbmZhcm0gUGF5cm9sbHMiLCB4bGFiID0gIk1vbnRocyAoc2luY2UgSmFudWFyeSAxOTM5KSIsIHlsYWIgPSAiTnVtYmVyIG9mIFBheXJvbGxzIikKYGBgCgoKIyMjIyBOb3QgU2Vhc29uYWxseSBBZGp1c3RlZCAoUEFZTlNBKQpgYGB7ciBvdXQud2lkdGggPSAiNzAlIiwgZHBpID0gNDAwfQpQQVlOU0EgPC0gcmVhZC5jc3YoZmlsZSA9ICJQQVlOU0EuY3N2IiwgaGVhZGVyID0gVFJVRSwgc2VwID0gIiwiKQpuZnBfbnNhX3RzIDwtIHRzKFBBWU5TQVsyXSkKcGxvdC50cyhuZnBfbnNhX3RzLCBtYWluID0gIlRvdGFsIE5vbmZhcm0gUGF5cm9sbHMgKE5vdCBTZWFzb25hbGx5IEFkanVzdGVkKSIsIHhsYWIgPSAiTW9udGhzIChzaW5jZSBKYW51YXJ5IDE5MzkpIiwgeWxhYiA9ICJOdW1iZXIgb2YgUGF5cm9sbHMiKQpgYGAKCgojIyMjIE5hcnJvd2luZyBPdXIgU2NvcGUKVGhyb3VnaG91dCB0aGUgODAgeWVhcnMgcmVwcmVzZW50ZWQgaW4gdGhlc2UgZGF0YXNldHMsIHZhcmlvdXMgZXZlbnRzIGhhdmUgb2NjdXJyZWQgdGhhdCBzaWduaWZpY2FudGx5IGNoYW5nZWQgdGhlIGNvbmRpdGlvbnMgb2YgdGhlIGVjb25vbXkuIEZvciB0aGlzIHJlYXNvbiwgd2Ugd2lsbCBsaW1pdCBvdXIgYW5hbHlzaXMgdG8gdGhlIHllYXJzIHRoYXQgZm9sbG93ZWQgdGhlIGZpbmFuY2lhbCBjcmlzaXMgb2YgMjAwNy8yMDA4LiBCeSBuYXJyb3dpbmcgb3VyIHNjb3BlIHRvIDIwMTAtMjAxOCwgd2UgYWltIHRvIHByb3ZpZGUgYSBtb3JlIHRlbGxpbmcgYW5hbHlzaXMgb2YgdGhlIHRyZW5kcyBhc3NvY2lhdGVkIHdpdGggdGhlIHBvc3QtcmVjZXNzaW9uIGVjb25vbWljIHJlY292ZXJ5LgoKIyMjIyBTZWFzb25hbGx5IEFkanVzdGVkIChQQVlFTVMpIDIwMTAtMjAxOApgYGB7ciBvdXQud2lkdGggPSAiNzAlIiwgZHBpID0gNDAwfQpuZnBfc2FfdHNfMjAxMF8yMDE4IDwtIHRzKFBBWUVNU1s4NTM6OTUxLCBdWzJdKQpwbG90LnRzKG5mcF9zYV90c18yMDEwXzIwMTgsIG1haW4gPSAiVG90YWwgTm9uZmFybSBQYXlyb2xscyAoU0EpLCAyMDEwLTIwMTgiLCB4bGFiID0gIk1vbnRocyAoc2luY2UgSmFudWFyeSAyMDEwKSIsIHlsYWIgPSAiTnVtYmVyIG9mIFBheXJvbGxzIikKYGBgCgojIyMjIE5vdCBTZWFzb25hbGx5IEFkanVzdGVkIChQQVlOU0EpIDIwMTAtMjAxOApgYGB7ciBvdXQud2lkdGggPSAiNzAlIiwgZHBpID0gNDAwfQpuZnBfbnNhX3RzXzIwMTBfMjAxOCA8LSB0cyhQQVlOU0FbODUzOjk1MSwgXVsyXSkKcGxvdC50cyhuZnBfbnNhX3RzXzIwMTBfMjAxOCwgbWFpbiA9ICJUb3RhbCBOb25mYXJtIFBheXJvbGxzIChOU0EpLCAyMDEwLTIwMTgiLCB4bGFiID0gIk1vbnRocyAoc2luY2UgSmFudWFyeSAyMDEwKSIsIHlsYWIgPSAiTnVtYmVyIG9mIFBheXJvbGxzIikKYGBgCgoKIyMjIENoYW5nZSBpbiBQYXlyb2xscwpGaXJzdCBvcmRlciBkaWZmZXJlbmNpbmcgb2YgU0EgYW5kIE5TQSBkYXRhCgojIyMjIFNBIERpZmZlcmVuY2VzIDIwMTAtMjAxOApgYGB7ciBvdXQud2lkdGggPSAiNzAlIiwgZHBpID0gNDAwfQpTQV9kaWZmIDwtIGRpZmYobmZwX3NhX3RzXzIwMTBfMjAxOCwgbGFnID0gMSwgZGlmZmVyZW5jZXMgPSAxKQpwbG90LnRzKFNBX2RpZmYsIG1haW4gPSAiU0EgRGlmZmVyZW5jZXMsIDIwMTAtMjAxOCIsIHhsYWIgPSAiTW9udGhzIChzaW5jZSBKYW51YXJ5IDIwMTApIiwgeWxhYiA9ICJOdW1iZXIgb2YgUGF5cm9sbHMiKQpgYGAKClRha2luZyB0aGUgZmlyc3QgZGlmZmVyZW5jZSBzZWVtcyB0byBoYXZlIGRldHJlbmRlZCB0aGUgb3JpZ2luYWwgdGltZSBzZXJpZXMuCgpgYGB7ciBvdXQud2lkdGggPSAiNzAlIiwgZHBpID0gNDAwfQpoaXN0KGFzLm51bWVyaWModW5saXN0KFNBX2RpZmYpKSwgYnJlYWtzPTE1LCBtYWluID0gIkhpc3RvZ3JhbSBvZiBTQSBQYXlyb2xsIGNoYW5nZXMiLCB4bGFiID0gIk51bWJlciBvZiBQYXlyb2xscyIpCmBgYAoKUGxvdHRpbmcgdGhpcyBoaXN0b2dyYW0gaW5kaWNhdGVzIHRoYXQgdGhlIGNoYW5nZSBpbiB0b3RhbCBzZWFzb25hbGx5IGFkanVzdGVkIHBheXJvbGxzIG1heSBmb2xsb3cgYSBsZWZ0LXNrZXdlZCBkaXN0cmlidXRpb24sIGNoYXJhY3Rlcml6ZWQgYnkgdGhlIGxvbmcgbGVmdCB0YWlsIGFib3ZlLiAKCgojIyMjIE5TQSBEaWZmZXJlbmNlcyAyMDEwLTIwMTgKYGBge3Igb3V0LndpZHRoID0gIjcwJSIsIGRwaSA9IDQwMH0KTlNBX2RpZmYgPC0gZGlmZihuZnBfbnNhX3RzXzIwMTBfMjAxOCwgbGFnID0gMSwgZGlmZmVyZW5jZXMgPSAxKQpwbG90LnRzKE5TQV9kaWZmLCBtYWluID0gIk5TQSBEaWZmZXJlbmNlcywgMjAxMC0yMDE4IiwgeGxhYiA9ICJNb250aHMgKHNpbmNlIEphbnVhcnkgMjAxMCkiLCB5bGFiID0gIk51bWJlciBvZiBQYXlyb2xscyIpCmBgYApgYGB7ciBvdXQud2lkdGggPSAiNzAlIiwgZHBpID0gNDAwfQpoaXN0KGFzLm51bWVyaWModW5saXN0KE5TQV9kaWZmKSksIGJyZWFrcz0xNSwgIG1haW4gPSAiSGlzdG9ncmFtIG9mIE5TQSBQYXlyb2xsIGNoYW5nZXMiLCB4bGFiID0gIk51bWJlciBvZiBQYXlyb2xscyIpCmBgYAoKU2ltaWxhcmx5LCBwbG90dGluZyB0aGlzIGhpc3RvZ3JhbSBpbmRpY2F0ZXMgdGhhdCB0aGUgY2hhbmdlIGluIHRvdGFsIG5vbi1zZWFzb25hbGx5IGFkanVzdGVkIHBheXJvbGxzIG1heSBhbHNvIGZvbGxvdyBhIGxlZnQtc2tld2VkIGRpc3RyaWJ1dGlvbiwgY2hhcmFjdGVyaXplZCBieSBhIGxvbmcgbGVmdCB0YWlsLiAKCgoKIyMjIyBTQSBEaWZmZXJlbmNlcyAyMDEwLTIwMTgKTmV4dCB3ZSBtZWFuLWNldG5lciB0aGUgU0FfZGlmZiB0aW1lIHNlcmllczogIAoKYGBge3Igb3V0LndpZHRoID0gIjcwJSIsIGRwaSA9IDQwMH0KU0FfbWVhbiA8LSBtZWFuKFNBX2RpZmYsIG5hLnJtID0gVFJVRSkKU0FfbWVhbgpjZW50ZXJlZF9TQV9kaWZmIDwtIFNBX2RpZmYgLSBTQV9tZWFuCnBsb3QudHMoY2VudGVyZWRfU0FfZGlmZiwgbWFpbiA9ICJDZW50ZXJlZCBTQSBEaWZmcywgMjAxMC0yMDE4IiwgeGxhYiA9ICJNb250aHMgKHNpbmNlIEphbnVhcnkgMjAxMCkiLCB5bGFiID0gIk51bWJlciBvZiBQYXlyb2xscyIpCmBgYAoKCgoK' target='_blank' title='User  at /Users/samchoi' download='project-nfp.Rmd'> &#8658; project-nfp.Rmd</a>  

### NFP EDA
We aim to explore two versions of NFP data: PAYEMS and PAYNSA. PAYEMS is a dataset with seasonally adjusted values, and PAYNSA is a dataset without seasonal adjustments. The data is recorded in thousands of persons (jobs created). The datasets contain monthly NFP report values from January 1939 to March 2018.  
<br>


#### Seasonally Adjusted (PAYEMS)

```r
PAYEMS <- read.csv(file = "PAYEMS.csv", header = TRUE, sep = ",")
nfp_sa_ts <- ts(PAYEMS[2])
plot.ts(nfp_sa_ts, main = "Seasonally Adjusted Total Nonfarm Payrolls", xlab = "Months (since January 1939)", ylab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-3-1.png" width="70%" />


#### Not Seasonally Adjusted (PAYNSA)

```r
PAYNSA <- read.csv(file = "PAYNSA.csv", header = TRUE, sep = ",")
nfp_nsa_ts <- ts(PAYNSA[2])
plot.ts(nfp_nsa_ts, main = "Total Nonfarm Payrolls (Not Seasonally Adjusted)", xlab = "Months (since January 1939)", ylab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-4-1.png" width="70%" />


#### Narrowing Our Scope
Throughout the 80 years represented in these datasets, various events have occurred that significantly changed the conditions of the economy. For this reason, we will limit our analysis to the years that followed the financial crisis of 2007/2008. By narrowing our scope to 2010-2018, we aim to provide a more telling analysis of the trends associated with the post-recession economic recovery.

#### Seasonally Adjusted (PAYEMS) 2010-2018

```r
nfp_sa_ts_2010_2018 <- ts(PAYEMS[853:951, ][2])
plot.ts(nfp_sa_ts_2010_2018, main = "Total Nonfarm Payrolls (SA), 2010-2018", xlab = "Months (since January 2010)", ylab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-5-1.png" width="70%" />

#### Not Seasonally Adjusted (PAYNSA) 2010-2018

```r
nfp_nsa_ts_2010_2018 <- ts(PAYNSA[853:951, ][2])
plot.ts(nfp_nsa_ts_2010_2018, main = "Total Nonfarm Payrolls (NSA), 2010-2018", xlab = "Months (since January 2010)", ylab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-6-1.png" width="70%" />


### Change in Payrolls
First order differencing of SA and NSA data

#### SA Differences 2010-2018

```r
SA_diff <- diff(nfp_sa_ts_2010_2018, lag = 1, differences = 1)
plot.ts(SA_diff, main = "SA Differences, 2010-2018", xlab = "Months (since January 2010)", ylab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-7-1.png" width="70%" />

Taking the first difference seems to have detrended the original time series.


```r
hist(as.numeric(unlist(SA_diff)), breaks=15, main = "Histogram of SA Payroll changes", xlab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-8-1.png" width="70%" />

Plotting this histogram indicates that the change in total seasonally adjusted payrolls may follow a left-skewed distribution, characterized by the long left tail above. 


#### NSA Differences 2010-2018

```r
NSA_diff <- diff(nfp_nsa_ts_2010_2018, lag = 1, differences = 1)
plot.ts(NSA_diff, main = "NSA Differences, 2010-2018", xlab = "Months (since January 2010)", ylab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-9-1.png" width="70%" />

```r
hist(as.numeric(unlist(NSA_diff)), breaks=15,  main = "Histogram of NSA Payroll changes", xlab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-10-1.png" width="70%" />

Similarly, plotting this histogram indicates that the change in total non-seasonally adjusted payrolls may also follow a left-skewed distribution, characterized by a long left tail. 



#### SA Differences 2010-2018
Next we mean-cetner the SA_diff time series:  


```r
SA_mean <- mean(SA_diff, na.rm = TRUE)
SA_mean
```

```
## [1] 188.0714
```

```r
centered_SA_diff <- SA_diff - SA_mean
plot.ts(centered_SA_diff, main = "Centered SA Diffs, 2010-2018", xlab = "Months (since January 2010)", ylab = "Number of Payrolls")
```

<img src="project-nfp_files/figure-html/unnamed-chunk-11-1.png" width="70%" />




