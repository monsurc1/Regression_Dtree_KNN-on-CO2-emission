# Regression_Dtree_KNN-on-CO2-emission

## **Regression Analysis**
### **1.1 Business Understanding**
	Dataset source: https://www.kaggle.com/datasets/sindhuinti/co2-emission 
	
	This set of data shows the details of the CO2 emissions by vehicles(cars) in Canada over a period of 7 years and originated from 
 	[open.canada.ca] website link.
	It seems that CO2 emissions can vary with the different features.
	
	As CO2 emission is one of the major environmental pollution issues in today’s world, I tried to explore the relationship between the features 
 	against the emission.
	
	Multiple linear regression models are performed on this dataset.

### **1.2 Data Understanding & Preparation**
	There are a total of 7385 rows and 12 columns. There are a few abbreviations that have been used to describe the features. I am listing them out here. 
 	The same can be found in the Data Description sheet.
	
 	Dataset attributes:
		• Car Make
		• Car Model
		• Vehicle(car) Class
		• Engine Size(L)
		• No. of. Cylinders
		• Transmission Type
		• Fuel Type ( X = Regular gasoline, Z = Premium gasoline, D = Diesel, E = Ethanol, N = Natural gas)
		• Fuel Consumption City (L/100 km)
		• Fuel Consumption Hwy (L/100 km) – (on Highway)
		• Fuel Consumption Comb (L/100 km) - (combined fuel consumption)
		• Fuel Consumption Comb (mpg) – (in mile per gallon)
  		• CO2 Emissions(g/km) – (in grams per kilometre)
![image](https://github.com/monsurc1/Regression_Dtree_KNN-on-CO2-emission/assets/7083845/219a4395-1ef8-4a28-a58e-88d25b98a6c2)

	So, we have 	- found 10310 instances in 12 attributes.
			- found no mussing value by using the describe() method.
	After renaming the column, it looks like this 
 ![image](https://github.com/monsurc1/Regression_Dtree_KNN-on-CO2-emission/assets/7083845/db5325ac-3b59-4107-8f60-c5cbba71159b)

 	More relevant data preparation is explained in the modelling part.
  ### **1.3 Modeling**
  	Found a good correlation between numeric attributes. I was interested in relationship between Co2 Emission and other features. 
   	I have used corr() method for this.

	Also, by using a scatter matrix plot, I have shown this relation.
	A promising linear model was seen.

 ![image](https://github.com/monsurc1/Regression_Dtree_KNN-on-CO2-emission/assets/7083845/8d1b504f-d944-4c4b-9b66-227545cc6161)

 	
  	I have prepared the dataset a little more by dropping some features. I was not interested in those features for the sake of this report.
  ![image](https://github.com/monsurc1/Regression_Dtree_KNN-on-CO2-emission/assets/7083845/649e89cc-5a85-4c56-81ca-7dc356e0719f)

  	Here, the dependent variable is Co2Emissions
  ![image](https://github.com/monsurc1/Regression_Dtree_KNN-on-CO2-emission/assets/7083845/f67e46cb-6b6a-423b-8594-bdf4fd76902d)

 	After this, I used the polynomial regression technique by using EngineSize data by squaring the values.
  ![image](https://github.com/monsurc1/Regression_Dtree_KNN-on-CO2-emission/assets/7083845/fcd41be4-7c12-4732-a22a-bbdc750d8fb1)

  ### **1.4 Evaluation**
	The results were found promising. With using a multiple regression model, RMSE was 18.254100098734245 whereas using a polynomial it is 18.05211896152715. 
 	So, RMSE has gone down by a fraction.
  	R square was 0.8981350998660036. Now, using the polynomial model it is 0.9003189081362316. Gone up.

   	So, we can say that the model is good enough for unseen data. 
    
    	**Our take from this project:** When the engine size is small the CO2 emission (air pollution) will be less. Where it is possible,
	we should not use bigger engines in our cars.


  



