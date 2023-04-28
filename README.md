# Practical-Test
Practical test by Dian Permana

##Answer##
# 1. Q1

Detail Can be check here : https://gist.github.com/DianPermana/e7ff8f3b8f622ecfc7ccd636b9f4c282 

# 2. Q2 Go to https://petstore.octoperf.com/actions/Catalog.action and report at least 3 bugs.


Feature : Search feature
   Given open https://petstore.octoperf.com/actions/Catalog.action
   And Input "Various Breeds" on search menu
   When I click Search button
   Then should be displayed product
   
   Result: Not Appear product "Various Breeds"
   Expected : Appear product
   
 2. Given After scenario 1
	When I refresh or click Reload this page
	Then Back to Main page
	
   Result: Still on the same page > Not Appear product "Various Breeds"
   Expected : Back to main page 
  
  Feature : flow transaction
 3. Given I already add 3 product on the shopping chart
	And Input Quantity from 3 to 99999
	And I click Update Cart
	When I input Quantiry again from 99999 to 3 
	Then the description should be true
	
			         | Item ID  | Product ID	              | Description	In Stock?	 | Quantity	| List Price |Total Cost
	  Result   : | AV-CB-01 | Adult Male Amazon Parrot  |	false	                 | 99999    | $193.50	 | $19,349,806.50
    Expected : | AV-CB-01 | Adult Male Amazon Parrot  |	true	                 | 99999    | $193.50	 | $19,349,806.50
