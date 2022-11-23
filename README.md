# BinTable-Collection

[![](https://developer.mastercard.com/_/_/src/global/assets/svg/mcdev-logo-dark.svg)](https://developer.mastercard.com/)


[![](https://github.com/Mastercard/oauth1-signer-java/workflows/Build%20&%20Test/badge.svg)](https://github.com/Mastercard/oauth1-signer-java/actions?query=workflow%3A%22Build+%26+Test%22)
## Overview

The repository contains a [Postman](https://www.postman.com/) collection for Mastercard's BinTable APIs.

###### *BIN (Bank Identification Number) refers to the first 6-8 digits on a card, also known as an Issuer Identification Number (IIN). It is the numeric standard for the identification of card-issuing financial entities in the payments industry. The BIN Table Resource (BTR) provides two distinct APIs, a full list of all available Mastercard BINs and the option to search for a filtered set using specific values.

#### What are we offering:
* A quick and easy way to start using Mastercard's BinTable APIs.
* Features provided by BinTable APIs.


## Before you run the collection
* You need your set of API keys. Refer to our [quick start guide](https://developer.mastercard.com/platform/documentation/getting-started-with-mastercard-apis/quick-start-guide/), if you don't already have one.
* Need to convert your private key to RSA-SHA256 format.
```
openssl pkcs12 -in '<location of the .p12 file>' | openssl rsa -out <Filename of the key generated ending with .key>
```

## Running the Collection

#### Step 1:
Download [collection⤓](./BinTableResource.postman_collection.json)and [environment⤓](./BinTable-ENV.postman_environment.json) and import this JSON your [Postman](https://www.postman.com/) 



#### OR 

[![Run in Postman](https://run.pstmn.io/button.svg)](https://god.gw.postman.com/run-collection/1044930-da4c5a13-c750-4730-977f-1ecdebb539f0?action=collection%2Ffork&collection-url=entityId%3D1044930-da4c5a13-c750-4730-977f-1ecdebb539f0%26entityType%3Dcollection%26workspaceId%3D8c3a90f5-cce1-46ec-839e-39f72964968a)

#### Step2: 
Select the _BinTable-STAGE_ environment (top right) and update `privateKey`and `consumerKey`.

#### Step3:
Click _Send_ on individual requests, or _Run collection_

## Supported use-cases

### Get all Bins
This API allows BTR Integrators (Merchants/Acquirers/Payment Service Providers - PSPs) to receive a list of all the most up-to-date BIN range information available from issuing banks. A BIN range update from an issuing bank is made available as soon as it is received on a daily basis.

### Account Search
This API allows BTR Integrators (Merchants/Acquirers/Payment Service Providers - PSPs/Fintechs) to search for BIN range information based on a key/value pair. The BIN Search API can be used any time by an BTR Integrator to get the keep BIN range information up-to-date in their system. A BIN range update from an issuing bank is made available as soon as it is received on a daily basis.
