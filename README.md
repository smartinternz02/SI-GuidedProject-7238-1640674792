# SI-GuidedProject-7238-1640674792
Project Airline Report 

1.	INTRODUCTION

1.1	Overview
Air passenger traffic forecast is of great importance for airlines and civil aviation authorities. For airlines, accurate forecasts play an increasingly important role in revenue management. It helps to reduce the airlines’ risk by objectively evaluating the demand of the air transportation business. For civil aviation authorities, air passenger traffic forecast provides a concrete basis for planning decisions in air transport infrastructure. Predicting as accurate as  possible  the passenger traffic for  a  certain  airport  is  an aspect  of major  importance  for both  the  airport management  and  the  airline  companies. The airport management must have  quality forecasts regarding the future passenger flow in  order  to  be  able  to  properly  decide  regarding  the  future  investments  in  the  airport infrastructure,  personnel  policy  and  airport  tariff  policy. Moreover,  airline  companies  use traffic forecasts to develop their strategy of operating new routes on certain destinations, to adapt  their  flight  frequencies  for  the  destinations  operated  and  to  establish  their  price policy. Thus, it is essential  that the model used for  predicting passenger traffic generates accurate  results  because  these  are  further  used  for  optimal  allocation  of  financial resources in various airport investments. 

1.2	Purpose

The main objective of this project is to build a prophet time series model that forecasts the passenger traffic for a given date. Predicting as accurate as possible the passenger traffic for a certain airport is an aspect of major importance for both the airport management and the airline companies. The theoretical quality of the forecasting models for air traffic of passengers is fundamental for obtaining the most accurate predictions. In this regard, a two-step process was used in developing the traffic forecasting model: (1) Identifying the proper regression model for traffic estimation based on the number of aircraft departures, and (2) Forecasting the number of aircraft departures for the current routes
Predicting as accurate as possible the passenger traffic 
for a certain airport is an aspect of major importance for both the airport management and the airline 
companies.  The  theoretical  quality  of  the  forecasting  models  for  air  traffic  of  passengers  is 
fundamental for obtaining the most accurate predictions. In this regard, a two-step process was used 
in  developing  the  traffic  forecasting  model:  (1)  Identifying  the  proper  regression  model  for  traffic 
estimation  based  on the  number  of  aircraft  departures,  and (2)  Forecasting  the  number of  aircraft 
departures for  the  current  routes 



2.	LITERATURE SURVEY

2.1	Existing Problem
The  theoretical  quality  of  the  forecasting  models  for  air  traffic  of  passengers  is fundamental  for  obtaining  the most  accurate  predictions.  Existing  models  for  predicting passenger air traffic are divided into several categories:
-	Parametric models  (econometric  models).
Multiple  regression models  built on the  relationship  between passenger  traffic  and  economic,  social,  demographic variables are intensely used as well as gravity models. Gravity models’ premise is that the passenger is informed and acts rationally from an  economic  point  of  view.  In  this  regard,  the  factors  that  influence  the  passenger’s behavior to choose a particular airport are: arrival time at the airport, frequency of flights to specific destinations, and flight ticket cost (Brian Graham, 1999).
This  category  also  includes  the  traffic  forecasting  methodology  used  by  IATA, which  estimates  the  market  air  demand  based  on  the  socio-economic  variables  of  the market,  GDP  and  adjustment  factors:  regulations,  demand,  airlines,  competition, substitution  (Air  Traffic  Forecasting  Methodology  by  IATA).  It  has  been  concluded  that there  is  generally  unidirectional  Granger  causality  from  GDP  to  Revenue  passenger Kilometers (RPK), also used as airline traffic (E. Fernandez, R.R. Pacheco, 2010). Wenbin Wei and Mark Hansen have used a logarithmic function for estimating the demand  of  passenger  air  traffic  based  on  the  following  independent  variables:  flight frequencies, number of seats in the aircraft, ticket price, flight distance, number of spokes in  the  network,  airport  capacity,  airport  area  population  income,  number  of  local passengers  who  travel  from  spoke  S  to  hub  H  by  airline  A,  total  number  of  initiated passenger  trips  originating  from  spoke  S  (Wenbin  Wei,  Mark  Hansen,  2006).  A  similar model, called the  Econometric Dynamic  Model  (EDM) was used to  predict the number  of  passengers  according  to  economic variables,  active  population,  consumer  price  index, number of flights, average occupancy rate of hotels, value foreign currency exchange rates values  at  international  arrivals  (Rafael  Bernardo  Carmona-Benítez,  Maria  Rosa  Nieto, Danya Miranda, 2016). The mixed multinomial logit model (MMNL) has  also  been used  with good results to analyze air travel behavior in airport choice (Stephane Hess, John W. Polak, 2005). Fuzzy  regression  analyses  is  used  for  estimating  passenger  air  traffic,  but  also  for forecasting  cargo  air  traffic  in  order  to  reduce  the  residual  value  resulting  from  the influence of ncertain and unidentified factors in parametric models (T.Y Chou, G.S Liang, T.C Han, 2011; M.S. Liao, G. S. Liang, C. Y. Chen, 2012; V.A Profillidis, 2000). Similar  with  the  multivariate  regression  model  is  the  ARIMAX  model  (Wai  Hong Kan Tsui,  Hatice  Ozer Balli,  Andrew Gilbey, Hamish Gow,  2014)  which  can  mprove the forecast accuracy by considering the autocorrelation which may exist within the regression 
residuals. 
-	Nonparametric  models,  namely  time  series  analysis
time  series  analysis  eliminates  the shortcomings of the parametric  methods of identifying and predicting all variables that influence the passenger traffic. Univariate  models  of  time  series  use  only  the  passenger  traffic  past  data  without considering  other  exogenous  variables.  These  time-sequence  models  generate  better predictive results, according to the study by Ya-Ling Huang and Chin - Tsai Lin who used The Gray Envelope Prediction Model (GEPM) for monthly, seasonal and annual passenger traffic  forecasts  (Ya-Ling Huang  , Chin  -  Tsai  Lin,  2011).  The  Grey prediction  model  is
suitable  for  short-term  forecasts  that  do  not  have a  high  degree  of  uncertainty. A  Grey - Markov  model  was  applied  by  Zhang  Wei,  Zhu  Jinfu  in  2009  in  order  to  estimate passenger  traffic  by  integrating  the  Grey  model  (used  for  short  periods  with  low uncertainty) in the Markov chain model applicable in dynamic settings. 
ARIMA autoregressive  model is suitable for  short term forecasts  and  when traffic 
records regular variations, cyclical seasonality, but generates significant errors when traffic variations  are  irregular (ACRP,  2007;  M.  Çuhadar,  2014;  A.  Danesi,  L. Mantecchini,  F. Paganelli, 2017). The SARIMA model is a combination of stochastic seasonal model and ARIMA model and can best describe the fluctuation of passenger flow of the airport terminal which presents a periodic  fluctuation.  The  study  carried  out  by  Ziyu  Li  et  al  using  SARIMA  generated predictions of passenger traffic very close to the actual values, the error rate of the model being between 1% and 3% (Ziyu Li, Jun Bi, Zhiyin Li, 2017). Another study developed by Wai  Hong  Kan  Tsui  et  al  for  predicting  passenger  traffic  at  Hong  Kong  airport  using SARIMA  and  ARIMAX  models  has  resulted  in  high  accuracy,  with  very  small  prediction errors (Wai Hong Kan Tsui, Hatice Ozer Balli, Andrew Gilbey, Hamish Gow, 2014). For  time  series  characterized  by  nonlinearity  with  irregular  fluctuations  and evolutions,  it  is  recommended  to  use  artificial  neural  networks  (ANNs),  support  vector machines  (SVMs),  genetic  programming  (GP)  and  ensemble  empirical  mode decomposition (EEMD) (Y. Bao, T Xiong, Z. Hu, 2012). The LSTM  (long short-term  memory) network  model, a  neural network  prediction model is proper for short-term traffic forecasting (Z. Zhao, W. Chen, X. Wu,  P.C.Y. Chen, Jingmeng  Li,  2017).  Neural  network  forecasting  models  are  also  used  if  there  is  a nonlinear relationship between the models’ variables (T.O. Blinova, 2007)





2.2	Proposed Solution
We will be building a Web application  where
•	The user selects the date from User Interface(UI)
•	The passenger traffic for the selected date  is analysed by the model 
•	The count  of  passengers for the selected date is displayed on UI
To accomplish this, complete all the milestones & activities listed below.
•	Installation of Pre-requisites.
o	Installation of Anaconda IDE / Anaconda Navigator.
o	Installation of Python packages.
•	Data Collection.
o	Create or Collect the dataset.
•	Data Pre-processing.
o	Importing of Libraries.
o	Importing of Dataset & Visualisation.
•	Model Building.
o	Fitting the prophet library.
o	Cross validation of the model.
o	Evaluation of the model.
o	Save the model.
•	Application Development.



3.	THEORITICAL ANALYSIS

3.1	Block Diagram
 

3.2	Hardware/Software Designing
Softwares are :
a.	Jubiter notebook
b.	Watson studio
c.	Virtual studio code
d.	Anaconda promt 
e.	Spider code	
Hardwares are :
a.	Windows 7 to 11
b.	Ram about 8 gb
c.	Intel core 5 or 7 or amd 5 
4.	EXPERIMENTAL INVESTIGATIONS
 
 
 
 

5.	FLOWCHART                        

 


6.	RESULT
For airlines, accurate forecasts play an increasingly important role in revenue management. It helps to reduce the airlines’ risk by objectively evaluating the demand of the air transportation business. For civil aviation authorities, air passenger traffic forecast provides a concrete basis for planning decisions in air transport infrastructure.

7.	ADVANTAGES & DISADVANTAGES

B.	Advantages
By accurately forecasting demand for each flight or seat, revenue management adjusts pricing to maximise unit revenue. By predicting when demand is high and relatively inelastic, lower fares can be restricted; by anticipating when demand is low but elastic, lower fares can be made more available.

C.	Disadvantages
It is normally accepted that even though there are difficulties associated with making forecasts of air transport demand, estimates are necessary to:
i.	Assist manufacturers in industry to anticipate levels of aircraft orders and to develop new aircraft.
ii.	Aid airlines in their short and long term planning for equipment, facilities and personnel.
iii.	Assist central governments to facilitate the orderly development of the national and international airways system
iv.	Aid all level of government and airport authorities in the planning of airport infrastructure including terminal facilities, access routes, runways, taxiways, aprons, support facilities and terminal air traffic control.
8.	APPLICATIONS
forecasting is a key tool for decision making, enabling anticipation to make short term decisions and how to respond to them as well as supporting longer term decisions with regard to future patterns in demand for air travel.
Forecasting is an important factor to any businesses because it gives the ability to make informed business decisions and establish data-driven strategies. It allows companies to have the capability to decide on the strategic allocation of resources, decide the need for corrective actions, or to adjust current strategies to reflect new situations. It is vital for companies to be always planning ahead to ensure the readiness to take on future demands as well as challenges and this is no different for companies in the aviation industry, particularly in this pandemic crisis downturn.



CONCLUSION

Passenger traffic is  one of  the most  important  factors which  guides  the  strategic 
and tactical decisions of both the airport and airline company management. In this regard, accurate estimation of passenger traffic will optimize an airport’s financial planning for the periods  to  come.  The  present  paper  describes  a  prediction  model  of  passenger  traffic. 



9.	FUTURE SCOPE
Using this, we will be able to understand:
•	How Prophet can be used to make time series forecasts
•	How to analyse trends and seasonal fluctuations using Prophet
•	The importance of changepoints in determining model accuracy


10.	BIBLIOGRAPHY
-	Additive and multiplicative seasonality — can you identify them correctly?
-	data.world: Air Traffic Passenger Data (Original Source: San Francisco Open Data)
-	GitHub: facebook/prophet
-	Airport Cooperative Research Program (ACRP), (2007). Airport Aviation Activity Forecasting.
-	Antonio  Danesi,  Luca  Mantecchini  and  Filippo  Paganelli,  (2017).  Long-Term  And  Short-Term
-	





