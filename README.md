[![Build Status](https://travis-ci.org/trifonnt/ext-lib-amazon-mws-orders.png?branch=master)](https://travis-ci.org/trifonnt/ext-lib-amazon-mws-orders)
[![](https://jitpack.io/v/trifonnt/ext-lib-amazon-mws-orders.svg)](https://jitpack.io/#trifonnt/ext-lib-amazon-mws-orders)


Amazon MWS(Marketplace Web Service) Orders Java Library - Version 2013-09-01.V293334172
=============================================================================== 
The project is mavenised unofficial copy of Java library provided by Amazon for dealing with Amazon Marketplace Web Service API.

 - https://developer.amazonservices.com/doc/orders/orders/v20130901/java.html

 - https://docs.developer.amazonservices.com/en_US/orders/2013-09-01/index.html

Current CI status: https://travis-ci.org/trifonnt/ext-lib-amazon-mws-orders



About this Library
=============================================================================== 

Based on the 2013-09-01 API version.
Refers only to the [MWSOrdersJavaClientLibrary-2013-09-01.zip](https://images-na.ssl-images-amazon.com/images/G/01/mwsportal/clientlib/Orders/2013-09-01/MWSOrdersJavaClientLibrary-2013-09-01._V293334172_.zip) file.


Prerequisites
=============================================================================== 

- Amazon Pro Merchant seller account or another Amazon account that makes you eligible to use Amazon Marketplace Web Service (Amazon MWS). For more information, see the [Amazon MWS FAQ](https://developer.amazonservices.com/gp/mws/faq.html).

- Registering for Amazon MWS. For more information see the [Amazon MWS FAQ](https://developer.amazonservices.com/gp/mws/faq.html).

- Java Platform Standard Edition 6.0 Development Kit (JDK 1.6.0_19) or newer. If your version of the JDK is older than 6.0, you must install the newer version. For more information, go to the Java SE Downloads page. 


## How to

### Migrate to new version of Amazon MWS Orders library
```shell
$ git clone https://github.com/trifonnt/ext-lib-amazon-mws-orders.git

$ cd ext-lib-amazon-mws-orders

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


$ mvn clean install -Dmaven.javadoc.skip=true -DskipTests=true
```

### Publish new version to JitPack

 - Create new Release in GitHub

 - Open below URL in order to start JitPack build process

```shell
https://jitpack.io/com/github/trifonnt/ext-lib-amazon-mws-orders/1.0.0-alpha.5
```

### Get this project into your Maven build(pom.xml)
```xml
...
	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
 ...
 ...
 	<dependency>
	    <groupId>com.github.trifonnt</groupId>
	    <artifactId>ext-lib-amazon-mws-orders</artifactId>
	    <version>1.0.0</version>
	</dependency>
...
```

Licensing
=============================================================================== 

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
