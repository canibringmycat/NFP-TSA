---
title: "Project NFP"
author: "Sam Choi, Eric Xu"
output:
  html_document:
    fig_height: 3
    fig_width: 5
    keep_md: true
  pdf_document: default
  word_document: default
---
<!-- Don't edit in between this line and the one below -->

*Source file* 
<a href='data:text/x-markdown;base64,LS0tCnRpdGxlOiAiUHJvamVjdCBORlAiCmF1dGhvcjogIlNhbSBDaG9pLCBFcmljIFh1IgpvdXRwdXQ6CiAgaHRtbF9kb2N1bWVudDoKICAgIGZpZ19oZWlnaHQ6IDMKICAgIGZpZ193aWR0aDogNQogICAga2VlcF9tZDogdHJ1ZQogIHBkZl9kb2N1bWVudDogZGVmYXVsdAogIHdvcmRfZG9jdW1lbnQ6IGRlZmF1bHQKLS0tCjwhLS0gRG9uJ3QgZWRpdCBpbiBiZXR3ZWVuIHRoaXMgbGluZSBhbmQgdGhlIG9uZSBiZWxvdyAtLT4KYGBge3IgaW5jbHVkZT1GQUxTRX0KbGlicmFyeShEYXRhQ29tcHV0aW5nKQpsaWJyYXJ5KGFzdHNhKQpgYGAKKlNvdXJjZSBmaWxlKiAKYGBge3IsIHJlc3VsdHM9J2FzaXMnLCBlY2hvPUZBTFNFfQppbmNsdWRlU291cmNlRG9jdW1lbnRzKCkKYGBgCgojIyMgTkZQIEVEQQpXZSBhaW0gdG8gZXhwbG9yZSB0d28gdmVyc2lvbnMgb2YgTkZQIGRhdGE6IFBBWUVNUyBhbmQgUEFZTlNBLiBQQVlFTVMgaXMgYSBkYXRhc2V0IHdpdGggc2Vhc29uYWxseSBhZGp1c3RlZCB2YWx1ZXMsIGFuZCBQQVlOU0EgaXMgYSBkYXRhc2V0IHdpdGhvdXQgc2Vhc29uYWwgYWRqdXN0bWVudHMuIFRoZSBkYXRhIGlzIHJlY29yZGVkIGluIHRob3VzYW5kcyBvZiBwZXJzb25zIChqb2JzIGNyZWF0ZWQpLiBUaGUgZGF0YXNldHMgY29udGFpbiBtb250aGx5IE5GUCByZXBvcnQgdmFsdWVzIGZyb20gSmFudWFyeSAxOTM5IHRvIE1hcmNoIDIwMTguICAKPGJyPgoKCiMjIyMgU2Vhc29uYWxseSBBZGp1c3RlZCAoUEFZRU1TKQpgYGB7ciBvdXQud2lkdGggPSAiNzAlIiwgZHBpID0gNDAwfQpQQVlFTVMgPC0gcmVhZC5jc3YoZmlsZSA9ICJQQVlFTVMuY3N2IiwgaGVhZGVyID0gVFJVRSwgc2VwID0gIiwiKQpuZnBfc2FfdHMgPC0gdHMoUEFZRU1TWzJdKQpwbG90LnRzKG5mcF9zYV90cywgbWFpbiA9ICJTZWFzb25hbGx5IEFkanVzdGVkIFRvdGFsIE5vbmZhcm0gUGF5cm9sbHMiLCB4bGFiID0gIk1vbnRocyAoc2luY2UgSmFudWFyeSAxOTM5KSIsIHlsYWIgPSAiTnVtYmVyIG9mIFBheXJvbGxzIikKYGBgCgoKCiMjIyMgTm90IFNlYXNvbmFsbHkgQWRqdXN0ZWQgKFBBWU5TQSkKYGBge3Igb3V0LndpZHRoID0gIjcwJSIsIGRwaSA9IDQwMH0KUEFZTlNBIDwtIHJlYWQuY3N2KGZpbGUgPSAiUEFZTlNBLmNzdiIsIGhlYWRlciA9IFRSVUUsIHNlcCA9ICIsIikKbmZwX25zYV90cyA8LSB0cyhQQVlOU0FbMl0pCnBsb3QudHMobmZwX25zYV90cywgbWFpbiA9ICJUb3RhbCBOb25mYXJtIFBheXJvbGxzIChOb3QgU2Vhc29uYWxseSBBZGp1c3RlZCkiLCB4bGFiID0gIk1vbnRocyAoc2luY2UgSmFudWFyeSAxOTM5KSIsIHlsYWIgPSAiTnVtYmVyIG9mIFBheXJvbGxzIikKYGBgCgoKIyMjIyBOYXJyb3dpbmcgT3VyIFNjb3BlClRocm91Z2hvdXQgdGhlIDgwIHllYXJzIHJlcHJlc2VudGVkIGluIHRoZXNlIGRhdGFzZXRzLCB2YXJpb3VzIGV2ZW50cyBoYXZlIG9jY3VycmVkIHRoYXQgc2lnbmlmaWNhbnRseSBjaGFuZ2VkIHRoZSBjb25kaXRpb25zIG9mIHRoZSBlY29ub215LiBGb3IgdGhpcyByZWFzb24sIHdlIHdpbGwgbGltaXQgb3VyIGFuYWx5c2lzIHRvIHRoZSB5ZWFycyB0aGF0IGZvbGxvd2VkIHRoZSBmaW5hbmNpYWwgY3Jpc2lzIG9mIDIwMDcvMjAwOC4gQnkgbmFycm93aW5nIG91ciBzY29wZSB0byAyMDEwLTIwMTgsIHdlIGFpbSB0byBwcm92aWRlIGEgbW9yZSB0ZWxsaW5nIGFuYWx5c2lzIG9mIHRoZSB0cmVuZHMgYXNzb2NpYXRlZCB3aXRoIHRoZSBwb3N0LXJlY2Vzc2lvbiBlY29ub21pYyByZWNvdmVyeS4KCiMjIyMgU2Vhc29uYWxseSBBZGp1c3RlZCAoUEFZRU1TKSAyMDEwLTIwMTgKYGBge3Igb3V0LndpZHRoID0gIjcwJSIsIGRwaSA9IDQwMH0KbmZwX3NhX3RzXzIwMTBfMjAxOCA8LSB0cyhQQVlFTVNbODUzOjk1MSwgXVsyXSkKcGxvdC50cyhuZnBfc2FfdHNfMjAxMF8yMDE4LCBtYWluID0gIlRvdGFsIE5vbmZhcm0gUGF5cm9sbHMgKFNBKSwgMjAxMC0yMDE4IiwgeGxhYiA9ICJNb250aHMgKHNpbmNlIEphbnVhcnkgMjAxMCkiLCB5bGFiID0gIk51bWJlciBvZiBQYXlyb2xscyIpCmBgYAoKIyMjIyBOb3QgU2Vhc29uYWxseSBBZGp1c3RlZCAoUEFZTlNBKSAyMDEwLTIwMTgKYGBge3Igb3V0LndpZHRoID0gIjcwJSIsIGRwaSA9IDQwMH0KbmZwX25zYV90c18yMDEwXzIwMTggPC0gdHMoUEFZTlNBWzg1Mzo5NTEsIF1bMl0pCnBsb3QudHMobmZwX25zYV90c18yMDEwXzIwMTgsIG1haW4gPSAiVG90YWwgTm9uZmFybSBQYXlyb2xscyAoTlNBKSwgMjAxMC0yMDE4IiwgeGxhYiA9ICJNb250aHMgKHNpbmNlIEphbnVhcnkgMjAxMCkiLCB5bGFiID0gIk51bWJlciBvZiBQYXlyb2xscyIpCmBgYAoKCiMjIyBDaGFuZ2UgaW4gUGF5cm9sbHMKRmlyc3Qgb3JkZXIgZGlmZmVyZW5jaW5nIG9mIFNBIGFuZCBOU0EgZGF0YQoKIyMjIyBTQSBEaWZmZXJlbmNlcyAyMDEwLTIwMTgKYGBge3Igb3V0LndpZHRoID0gIjcwJSIsIGRwaSA9IDQwMH0KU0FfZGlmZiA8LSBkaWZmKG5mcF9zYV90c18yMDEwXzIwMTgsIGxhZyA9IDEsIGRpZmZlcmVuY2VzID0gMSkKcGxvdC50cyhTQV9kaWZmLCBtYWluID0gIlNBIERpZmZlcmVuY2VzLCAyMDEwLTIwMTgiLCB4bGFiID0gIk1vbnRocyAoc2luY2UgSmFudWFyeSAyMDEwKSIsIHlsYWIgPSAiTnVtYmVyIG9mIFBheXJvbGxzIikKYGBgCgpUYWtpbmcgdGhlIGZpcnN0IGRpZmZlcmVuY2Ugc2VlbXMgdG8gaGF2ZSBkZXRyZW5kZWQgdGhlIG9yaWdpbmFsIHRpbWUgc2VyaWVzLgoKYGBge3Igb3V0LndpZHRoID0gIjcwJSIsIGRwaSA9IDQwMH0KaGlzdChhcy5udW1lcmljKHVubGlzdChTQV9kaWZmKSksIGJyZWFrcz0xNSwgbWFpbiA9ICJIaXN0b2dyYW0gb2YgU0EgUGF5cm9sbCBjaGFuZ2VzIiwgeGxhYiA9ICJOdW1iZXIgb2YgUGF5cm9sbHMiKQpgYGAKClBsb3R0aW5nIHRoaXMgaGlzdG9ncmFtIGluZGljYXRlcyB0aGF0IHRoZSBjaGFuZ2UgaW4gdG90YWwgc2Vhc29uYWxseSBhZGp1c3RlZCBwYXlyb2xscyBtYXkgZm9sbG93IGEgbGVmdC1za2V3ZWQgZGlzdHJpYnV0aW9uLCBjaGFyYWN0ZXJpemVkIGJ5IHRoZSBsb25nIGxlZnQgdGFpbCBhYm92ZS4gCgoKIyMjIyBOU0EgRGlmZmVyZW5jZXMgMjAxMC0yMDE4CmBgYHtyIG91dC53aWR0aCA9ICI3MCUiLCBkcGkgPSA0MDB9Ck5TQV9kaWZmIDwtIGRpZmYobmZwX25zYV90c18yMDEwXzIwMTgsIGxhZyA9IDEsIGRpZmZlcmVuY2VzID0gMSkKcGxvdC50cyhOU0FfZGlmZiwgbWFpbiA9ICJOU0EgRGlmZmVyZW5jZXMsIDIwMTAtMjAxOCIsIHhsYWIgPSAiTW9udGhzIChzaW5jZSBKYW51YXJ5IDIwMTApIiwgeWxhYiA9ICJOdW1iZXIgb2YgUGF5cm9sbHMiKQpgYGAKYGBge3Igb3V0LndpZHRoID0gIjcwJSIsIGRwaSA9IDQwMH0KaGlzdChhcy5udW1lcmljKHVubGlzdChOU0FfZGlmZikpLCBicmVha3M9MTUsICBtYWluID0gIkhpc3RvZ3JhbSBvZiBOU0EgUGF5cm9sbCBjaGFuZ2VzIiwgeGxhYiA9ICJOdW1iZXIgb2YgUGF5cm9sbHMiKQpgYGAKClNpbWlsYXJseSwgcGxvdHRpbmcgdGhpcyBoaXN0b2dyYW0gaW5kaWNhdGVzIHRoYXQgdGhlIGNoYW5nZSBpbiB0b3RhbCBub24tc2Vhc29uYWxseSBhZGp1c3RlZCBwYXlyb2xscyBtYXkgYWxzbyBmb2xsb3cgYSBsZWZ0LXNrZXdlZCBkaXN0cmlidXRpb24sIGNoYXJhY3Rlcml6ZWQgYnkgYSBsb25nIGxlZnQgdGFpbC4gCgoKCiMjIyMgU0EgRGlmZmVyZW5jZXMgMjAxMC0yMDE4Ck5leHQgd2UgbWVhbi1jZXRuZXIgdGhlIFNBX2RpZmYgdGltZSBzZXJpZXM6ICAKCmBgYHtyIG91dC53aWR0aCA9ICI3MCUiLCBkcGkgPSA0MDB9ClNBX21lYW4gPC0gbWVhbihTQV9kaWZmLCBuYS5ybSA9IFRSVUUpClNBX21lYW4KY2VudGVyZWRfU0FfZGlmZiA8LSBTQV9kaWZmIC0gU0FfbWVhbgpwbG90LnRzKGNlbnRlcmVkX1NBX2RpZmYsIG1haW4gPSAiQ2VudGVyZWQgU0EgRGlmZnMsIDIwMTAtMjAxOCIsIHhsYWIgPSAiTW9udGhzIChzaW5jZSBKYW51YXJ5IDIwMTApIiwgeWxhYiA9ICJOdW1iZXIgb2YgUGF5cm9sbHMiKQpgYGAKCgoKCg==' target='_blank' title='User  at /Users/Eric' download='project-nfp.Rmd'> &#8658; project-nfp.Rmd</a>  

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




