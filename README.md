# Practical-Test / Written Assignment


# 1. Q1 Create a test scenario which has multiple test cases for the following features:
```
1. As a user, I want to create a public gist.	
2. As a user, I want to edit an existing gist.	
3. As a user, I want to delete an existing gist.	

The test cases should include as much detail as possible.
```

Detail Can be check here : https://gist.github.com/DianPermana/00fd30b7c5065875c2337ad6ffbc6d1e

# 2. Q2 Go to https://petstore.octoperf.com/actions/Catalog.action and report at least 3 bugs.

```
Feature : Search feature
   Given open https://petstore.octoperf.com/actions/Catalog.action
   And Input "Birds" on search menu
   When I click Search button
   Then should be displayed all birds product
   
   **Result   : Not Appear product "Birds"**
   **Expected : Appear all product "Birds"**
   
   Given After scenario 1
   When I refresh or click Reload this page
   Then Back to Main page
	
   Result   : Still on the same page > Not Appear product "Birds"
   Expected : Back to main page 
  
  
 Feature : Add to cart
   Given I am on "https://petstore.octoperf.com/actions/Cart.action"
   And I Click "Fish" Categories 
   And I Click "FI-SW-01" Product ID with "Anglefish"name
   When click button Add to cart "FI-SW-01" with description "Large Angelfish"
   Then Should be succesfully add to chart 
     
   **Result   : Failed add to cart**
   **Expected : succesfull add to cart**
	
 Feature : flow transaction
   Given I already add 3 product on the shopping chart
   And Input Quantity from 3 to 99999
   And I click Update Cart
   When I input Quantiry again from 99999 to 3 
   Then the description should be true
	
	       | Item ID  | Product ID	              | Description In Stock?	 | Quantity	| List Price     | Total Cost
    Result   : | AV-CB-01 | Toothless Tiger Shark     |	false	                 | 9999         | $18.50	 | $184.981.50
    Expected : | AV-CB-01 | Adult Male Amazon Parrot  |	true	                 | 9999         | $18.50	 | $184.981.50
```

Evidence Result testing

https://user-images.githubusercontent.com/18004033/235273419-42259705-b901-4fd0-a678-63d2b4e324a7.mp4


# 3. Q3 Below is a public API doc listing a collection of API endpoints related to Countries. https://restcountries.com/#api-endpoints-v3-all


Script test can be check here : https://github.com/DianPermana/Practical-Test/blob/main/Rest_Countries.jmx

Results API testing : 

https://user-images.githubusercontent.com/18004033/235127492-47b20517-978d-4345-bedf-46bb8cadb1a1.mp4

I use JMeter to create scenario testing, and divide it into two categories of scenario tests, namely positive cases and negative cases. Json Extractor as main sampler to extract data from response end point (https://restcountries.com/v3.1/name/{name}) and then store for all of the next process on other end point, so more easy for product team especially QA. if we want to change which country want to check. some end point issue especially for currency end point (https://restcountries.com/v3.1/currency/{currency}). The interesting thing about this testing is that I'm trying to create modular test scripts, so that by changing only 1 parameter, which is the country name, all endpoints can be run sequentially.

# 4. Q4 Are you familiar with Automation testing?
```
If yes, create an automation script using any framework of your choice for the below scenario:
1. Go to https://www.cermati.com/gabung
2. Enter all required fields (cover only positive cases) and register your account If no, canyou code in python or Javascript?
```

Yes, I have experience. Since the task automation is relatively simple, I opted to use JMeter as it is easier to use within a set framework. I am also accustomed to using pytest for automation, which can be viewed here: https://github.com/DianPermana/Automation-Testing-BDD


Results Automation testing : 

https://user-images.githubusercontent.com/18004033/235124869-b6dff3f4-1729-4d0a-bd68-2c9b829ff307.mp4


Tech stack : 

1. [x] java 17.0.5 2022-10-18 LTS
2. [x] Selenium 4
3. [x] Chrome driver.exe Version 112.0.5615.138 (Official Build) (64-bit)
4. [x] JMeter 5.5



