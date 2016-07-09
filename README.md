[![Build Status](https://travis-ci.org/trifonnt/amazon-mws-orders.png?branch=master)](https://travis-ci.org/trifonnt/amazon-mws-orders)

Amazon MWS(Marketplace Web Service) Orders Java Library - Version 2013-09-01.V293334172
=============================================================================== 
The project is mavenised unofficial copy of Java library provided by 
Amazon for dealing with Amazon Marketplace Web Service API.

https://developer.amazonservices.com/doc/orders/orders/v20130901/java.html

http://docs.developer.amazonservices.com/en_US/orders/2013-09-01/index.htlm

Current CI status: https://travis-ci.org/integration-technology/amazon-mws-orders


About this Library
=============================================================================== 

Based on the 2013-09-01 API version.
Refers only to the [MWSOrdersJavaClientLibrary-2013-09-01.zip](https://images-na.ssl-images-amazon.com/images/G/01/mwsportal/clientlib/Orders/2013-09-01/MWSOrdersJavaClientLibrary-2013-09-01._V293334172_.zip) file.


Prerequisites
=============================================================================== 

- Amazon Pro Merchant seller account or another Amazon account that makes you eligible to use Amazon Marketplace Web Service (Amazon MWS). For more information, see the Amazon MWS FAQ.

- Registering for Amazon MWS. For more information see the Amazon MWS FAQ.

- Java Platform Standard Edition 6.0 Development Kit (JDK 1.6.0_19) or newer. If your version of the JDK is older than 6.0, you must install the newer version. For more information, go to the Java SE Downloads page. 


Building when migrating to new Amazon MWS Order library version
===============================================================================

```shell
$ git clone https://github.com/trifonnt/amazon-mws-orders.git

$ cd amazon-mws-orders

$ mkdir orig-library

$ cd orig-library

$ wget https://images-na.ssl-images-amazon.com/images/G/01/mwsportal/clientlib/Orders/2013-09-01/MWSOrdersJavaClientLibrary-2013-09-01._V293334172_.zip

$ unzip MWSOrdersJavaClientLibrary-2013-09-01._V293334172_.zip


$ mv src/com/amazonservices/mws/orders/_2013_09_01/mock/*.xml ../src/test/resources/
$ mv src/com/amazonservices/mws/orders/_2013_09_01/mock/MarketplaceWebServiceOrdersMock.java ../src/test/java/com/amazonservices/mws/orders/_2013_09_01/mock/
$ rm src/com/amazonservices/mws/orders/_2013_09_01/mock -r

$ mv src/com/amazonservices/mws/orders/_2013_09_01/samples/*.java ../src/test/java/com/amazonservices/mws/orders/_2013_09_01/samples/
$ rm src/com/amazonservices/mws/orders/_2013_09_01/samples -r

$ mv src/com/amazonservices/mws/orders/_2013_09_01/*.java ../src/main/java/com/amazonservices/mws/orders/_2013_09_01
$ mv src/com/amazonservices/mws/orders/_2013_09_01/model/*.java ../src/main/java/com/amazonservices/mws/orders/_2013_09_01/model
$ rm -r src/com/amazonservices/mws/orders/_2013_09_01/model

$ mv runtime-src/com/amazonservices/mws/client/*.java ../src/main/java/com/amazonservices/mws/client


$ mvn clean install -Dmaven.javadoc.skip=true -DskipTests=true

```


Licensing
=============================================================================== 

This software is licensed under the terms you may find in the file
named "LICENSE.txt" in this directory.
