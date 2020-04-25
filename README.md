# spring-boot-mvc-jersey-jpa
This is a Jersey REST resource used in the Pluralsight course, Introduction to Integration With Apache Camel. This resource should be used with the camel-spring-jpa-order-fulfillment-processor repository. The app in the camel-spring-jpa-order-fulfillment-processor repository builds a Camel route and uses this Jersey resource as an endpoint. 

Start the service:

        mvn exec:java

The URL is: 

http://localhost:8090/services/orderFulfillment/processOrders

If you would like to test the service directly, you can use a plug-in to Firefox called Poster. Use the URL above, the content type as application/json and the following body:

{"orders":[
	{"firstName":"Tester","lastName":"Test","email":"test@test.com","orderNumber":"1234","timeOrderPlaced":"Dec 23, 2014 5:38:03 PM","orderItems":[
		{"itemNumber":"1234","price":12.3300000000000000710542735760100185871124267578125,"quantity":5}
	]}
]}

If the service call was successful, you should see the order information output to the command window and you should get a 200 for the response. 
