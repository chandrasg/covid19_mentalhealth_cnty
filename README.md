# Twitter estimates of County-level Mental Health

Mental health metrics, namely psychological stress, lonely expressions, anxiety, and sentiment are measured daily using pre-trained machine learning models applied to a random 1% Twitter data. For more details, read our publication in the Journal of General Internal Medicine: http://wwbp.org/papers/jgim-2020.pdf 

Data snapshot:
| group_id         	| feat      	| value 	| group_norm       	| day        	| cnty  	|
|------------------	|-----------	|-------	|------------------	|------------	|-------	|
| 2020-04-16:01001 	| ANX_SCORE 	| 78    	| 2.92268402613488 	| 2020-04-16 	| 01001 	|
| 2020-04-16:01003 	| ANX_SCORE 	| 830   	| 2.82928758282208 	| 2020-04-16 	| 01003 	|
| 2020-04-16:01005 	| ANX_SCORE 	| 13    	| 3.4083486715075  	| 2020-04-16 	| 01005 	|
| 2020-04-16:01017 	| ANX_SCORE 	| 93    	| 2.67820445675611 	| 2020-04-16 	| 01017 	|
| 2020-04-16:01021 	| ANX_SCORE 	| 96    	| 3.02387743147066 	| 2020-04-16 	| 01021 	|

`cnty`: FIPS code of county

`day`: date

`group_norm`: mental health estimate; a sum of term relative frequencies weighted by their association with this mental health outcome in the pre-trained model

`value`: number of words contributing to the estimate

`feat`: descriptor of metric

`group_id`: concatenation of `day`:`cnty`

This data (aggregated to the state-level) is also used to update the Penn COVID Twitter Map https://penncovid19hub.com/twitter-map 

## Citation
APA:
```
Guntuku, S. C., Sherman, G., Stokes, D. C., Agarwal, A. K., Seltzer, E., Merchant, R. M., & Ungar, L. H. (2020). Tracking Mental Health and Symptom Mentions on Twitter During COVID-19. Journal of general internal medicine, 1-3.
```
Bib:
```
@article{guntuku2020tracking,
  title={Tracking Mental Health and Symptom Mentions on Twitter During COVID-19},
  author={Guntuku, Sharath Chandra and Sherman, Garrick and Stokes, Daniel C and Agarwal, Anish K and Seltzer, Emily and Merchant, Raina M and Ungar, Lyle H},
  journal={Journal of general internal medicine},
  pages={1--3},
  year={2020},
  publisher={Springer}
}
```

Details of how these models were trained are described in the following papers:
Stress: 
```
Guntuku, S. C., Buffone, A., Jaidka, K., Eichstaedt, J. C., & Ungar, L. H. (2019, July). Understanding and measuring psychological stress using social media. In Proceedings of the International AAAI Conference on Web and Social Media (Vol. 13, No. 01, pp. 214-225).
```

Loneliness: 
```
Guntuku, S. C., Schneider, R., Pelullo, A., Young, J., Wong, V., Ungar, L., ... & Merchant, R. (2019). Studying expressions of loneliness in individuals using twitter: an observational study. BMJ open, 9(11).
```

Sentiment:
```
Mohammad, S. M., & Turney, P. D. (2013). Crowdsourcing a word–emotion association lexicon. Computational Intelligence, 29(3), 436-465.
```

For any queries, please reach out at `sharathg at cis dot upenn dot edu` or `garricks at sas dot upenn dot edu`.
