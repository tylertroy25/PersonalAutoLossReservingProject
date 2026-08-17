# Personal Auto Loss Reserving Model

## Overview
This workbook estimates unpaid loss reserves for a private passenger auto liability company using chain-ladder and Bornhuetter-Ferguson (BF) methods. Our models are based on 10 years of claims development data, with dollar amounts listed in thousands. Screenshots of the Excel workbook are provided here, so you don't have to download the whole file.

## Data
We sourced our data from the CAS-hosted NAIC Schedule P dataset. This set contains private passenger auto liability/medical information with claims between the years 1998-2007. From this dataset, we chose to focus on one specific company, Tennessee Farmers Mutual (GRCODE 6947). Tennessee Farmers was chosen as a mid-size regional writer that had ~$252M premium and a monotonic development pattern. For this reserving project, we used the cumulative paid losses for each accident year to calculate the expected unpaid loss reserves for recent and present years.

<img width="1090" height="252" alt="image" src="https://github.com/user-attachments/assets/8c1a322c-7c23-46af-a2bd-47e580f8ce4d" />

<img width="632" height="380" alt="image" src="https://github.com/user-attachments/assets/26dc1d64-8c6f-410c-bb77-30492421d4c2" />

## Chain Ladder Methodology
To start, we built a 10x10 claims development triangle and calculated the age-to-age factors for each accident year. We calculated both the volume-weighted average and simple average for each age-to-age band. Then, we selected the volume-weighted average as the basis for our future calculations as this is the standard approach and reduces the influence of smaller or noisier years. After that, we computed the cumulative development factors (CDFs) and applied these to the latest diagonal to project the ultimates and IBNR. This resulted in $146.10M total indicated IBNR.

<img width="895" height="254" alt="image" src="https://github.com/user-attachments/assets/8a84c914-7ded-4d5d-a5b9-f41c99f523ef" />

## Bornhuetter-Ferguson Methodology
After using the Chain-Ladder method, we also computed the IBNR using the BF method. This stabilizes the estimates for less mature accident years (like 2005-2007) as these are more sensitive to noise in the chain-ladder approach. In order to use the BF method, we first needed to calculate the expected loss ratio (ELR). To obtain this, we averaged the chain-ladder-implied loss ratios from the most mature accident years which resulted in a value of 0.7466. After carrying out the BF method with our ELR, we got a result of $144.22M total indicated IBNR.

<img width="1305" height="233" alt="image" src="https://github.com/user-attachments/assets/84fb4e15-d5c8-4eed-a796-0a76bddf4fa7" />

## Comparison
After running both the chain-ladder and BF method, we graphed the IBNR of the two for each accident year. As seen in the table accompanying the graph, both methods produce closely aligned results (within 1.3% of each other) with BF showing slightly lower figures. This does appear to be consistent with the BF's expected effect on the least mature accident years.

<img width="1614" height="373" alt="image" src="https://github.com/user-attachments/assets/ae291bad-3f16-48e1-b8a4-c66ea7cbe6ee" />

## Sensitivity Analysis
Our final test in this project was a comparison between using the volume-weighted CDFs and simple average CDFs. After running the simple average CDF methods, we found that there was only a 0.24% difference in total IBNR between the two methods. This shows that our reserve estimates aren't highly sensitive to our volume-weighted CDF assumption.

<img width="1026" height="359" alt="image" src="https://github.com/user-attachments/assets/bcd5c16e-cb62-4499-a030-6b7d844dff3b" />

## Limitations
There were a few limitations in this project. To start, this project is only for a single company compared to the entire private passenger auto industry. This project also does not consider case reserve development separately from paid case development. Finally, our ELR was derived from our data rather than externally validated. In real-world scenarios, ELRs are subject to change year-over-year. Overall, the close alignment between the chain-ladder and BF estimates, as well as the low sensitivity to factor selection supports our figures in the $144M-$146M reserve range as a reasonable estimation.
