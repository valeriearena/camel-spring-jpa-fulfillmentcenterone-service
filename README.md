# Fulfillment Center One Service

Start the service:

        mvn exec:java

This is the REST service for Fulfillment Center One in my Pluralsight Apache Camel course and should be used with the camel / spring app in the camel-spring-jpa-order-fulfillment-processor repository.

The URL is: 

http://localhost:8090/services/orderFulfillment/processOrders

If you would like to test the service directly, you can use a plug-in to Firefox called Poster. Use the URL above, the content type as application/json and the following body:

{"orders":[
	{"firstName":"Tester","lastName":"Test","email":"test@test.com","orderNumber":"1234","timeOrderPlaced":"Dec 23, 2014 5:38:03 PM","orderItems":[
		{"itemNumber":"1234","price":12.3300000000000000710542735760100185871124267578125,"quantity":5}
	]}
]}

If the service call was successful, you should see the order information output to the command window and you should get a 200 for the response. 
