# Extra Fee
## Overview

Magento currently only supports certain shipping methods: Free Shipping, Flat Rate, Table Rate, UPS, Magento Shipping, USPS, FedEx, DHL. If store owners want to add fees for any services in their store like gift wrap, fast shipment within 2 hours, etc, they can not be configured. Developed by Mageplaza, [Extra Fee module](https://www.mageplaza.com/magento-2-extra-fee/) allows shoppers to add whatever fees they want and display them on their Checkout and Shopping Cart pages.

## How to configure

From the Admin Panel, go to `Stores > Extra Fee > Configuration`

![extra fee](https://i.imgur.com/0P4gSBJ.png)

### 1. Configuration

From the Admin Panel, go to `Stores > Extra Fee > Configuration`, choose `General` sections

![extra fee1](https://i.imgur.com/qfQmWmN.png)

- **Enable**: Select Yes to use the feature of the module
- **Calculate Total includes**: Choose how to calculate the service cost
  - `Calculate Total includes = Discount`: the service fee includes the discount
  - `Calculate Total includes = Shipping Fee`: The service fee is calculated after shipping surcharge
  - `Calculate Total includes = Tax`: The service fee includes the tax of the product
  - Many options can be selected
  - Only apply this calculation method with the fee type as a percentage
  
### 2. Manage Extra Fees
#### How to Add New Rule

- Step 1: Enter the full information in thr General section
- Step 2: Set the conditions to apply the rule in the Condition section
- Step 3: Set the form, service fee, display area ... of the rule in Action section
- Step 4: Enter labels for service type for the store and in the backend

##### Step 1: Enter the full information in thr General section

- **Name**: Enter the name of the rule
- **Status**: Select "Enable" to apply the rule
- **Store Views**
  - Only selected stores are applied the rule
  - Multiple stores can be selected at the same time

- **Customer Groups**
  - Only selected customer group can see the rule
  - Multiple groups can be selected at the same time

- **Priority**
  - Enter the priority for applying the rule
  - The smaller the number, the higher the priority. For rules with equal priority, the priority will be based on ID.

![extra fee2](https://i.imgur.com/TLlSmPb.png)

##### Step 2: Set the conditions to apply the rule in the Condition section

- Select conditions to apply the rule
- You can set the conditions for the **Cart** or **Product** section as *Subtotal  greater than  50, Total Items Quantity  less than  5, etc*

![extra fee3](https://i.imgur.com/yMwCnDt.png)

##### Step 3: Set the form, service fee, display area ... of the rule in Action section

- **Apply Type**:

![extra fee4](https://i.imgur.com/QYCcCaq.png)

  - **Apply Type = Manual**: Customers can optionally choose the service type of the rule
    - `Display Area`: Choose the area to show the rule
    
![extra fee5](https://i.imgur.com/rAHAzPu.png)

  - `Display Area = Cart Summary`: Display the rule in the `Cart Summary` section
  - `Display Area = Shipping Method`: Display the rule in the `Shipping Method` section
  - `Display Area = Payment Method`: Display the rule in the `Payment Method` section

- **Display Type`: Choose the display type of the rule for customers to choose

![extra fee6](https://i.imgur.com/Ns1uxwt.png)

  - `Display Type = Radio`: Allow choosing the display type as radio
  - `Display type= Select`: Allow choosing the display type as select
  - `Display Type = Checkbox`: Allow choosing the display type as checkbox

- **Is Required**: Choose Yes to force customers to choose at least one service type.

- **Apply Type = Automatic**: Service type of the rule will be applied automatically.
  - `Fee Type`: Choose the fee type
  
  ![extra fee7](https://i.imgur.com/XL20wsa.png)
  
  - `Fee  Type = Percentage of cart total`: Service fee will be calculated as percentage of total cart
  - `Fee Type = Fixed amount for the whole cart`: Service fee will be charged as a certain amount when the customers purchase the products
  - `Fee Type = Fixed amount for each item`: The service fee will be calculated as a certain amount on each item in the cart

- **Fee Amount** 
  - Enter the amount or percentage (depending on the payment type you choose) to apply for the service fee
  - This field is not allowed to be empty
  
- **Fee Tax**:
  - Choose `Tax Rule` to calculate the fee tax for service fee
  - `Fee Tax = No`: Not apply to calculate the fee tax for service fee
  
- **Cart Sort Order**: 
  - Enther the priority for displaying the rule on the frontend and in the admin order
  - The smaller the input number, the higher the display priority. For the rule with equal priority, the priority will be based on the ID.
  
- **Refundable**:
  - Choose Yes to aplly the service fee for the refund order
  - The service fee will be applied at the first refund
  
- **Stop further processing**:
  - Choose Yes to limit the number of the rule that is applied for the service types (based on the priority and ID)
  - For example: There're 4 rules as Rule 1, Rule 2, Rule 3 and Rule 4 and the respective priority is 0, 5, 3 and 3.
    - All rules are set as `Stop further processing  = No: all rules are applied
    - Edit the Rule 3 and choose `Stop further processing = Yes`: After you Apply Ryle, the applied rules is Rule 1 (as the high priority) and Rule 3. Rule 2 (as the small priority) and Rule 4 (as creating later) are not applied.
    
    ![extra fee8](https://i.imgur.com/PeEUu1V.png)
     

##### Step 4: Enter labels for service types for the store and in the backend

- For **Apply Type = Manual**: Display the `Manage Option`
  - *Type*: Choose the service fee type
    - - `Fee  Type = Percentage of cart total`: Service fee will be calculated as percentage of total cart
    - `Fee Type = Fixed amount for the whole cart`: Service fee will be charged as a certain amount when the customers purchase the products
    - `Fee Type = Fixed amount for each item`: The service fee will be calculated as a certain amount on each item in the cart

  - *Amount*: Enter the amount or percentage (depending on the payment type you choose) to apply for the service fee
  - *Admin*: 
    - Enter the display name in the admin order/invoice/shipment/credit memo for the selected service type
    - This field is not allowed to be empty
    
  - *Stores*: Enter the display name for added service type on the frontend of the stores
  - *Is Default*: Choose the default service type when customers choose a new service
  - *New Option*: Click on the `New Option` button to setup other services
  
- For **Apply Type = Automatic**: Display the `Manage Labels`
  - *Admin*:
    - Enter the display name in the admin order/invoice/shipment/credit memo for selected service type
    - This field is not allowed to be empty
    
  - *Stores*: Enter the display name for selected service type on the frontend of the stores
  
  ![extra fee9](https://i.imgur.com/PJbQJuh.png)
  
## 3. Frontend
### 3.1. Display on the Cart Summary

![extra fee1](https://i.imgur.com/kJ0lC1i.png)

### 3.2. Display on the Payment Method

![extra fee11](https://i.imgur.com/N9iQAn8.png)

### 3.3. Display on the Shipping Methods
![extra fee12](https://i.imgur.com/lRq5pFG.png)

### 3.4. Display on the Order
![extra fee13](https://i.imgur.com/ZFe8K2n.png)

### 3.5. Display on the Invoice

![extra fee14](https://i.imgur.com/I6L4FIA.png)

### 3.6. Display on the Shipment

![extra fee15](https://i.imgur.com/qN8XCiz.png)

### 3.7 Display on the Credit Memo
![extra fee16](https://i.imgur.com/2mFf40A.png)


## 4. Backend
### 4.1. Order

![extra fee17](https://i.imgur.com/LZ9HbFJ.png)

### 4.2. Invoice
![extra fee18](https://i.imgur.com/zntETEa.png)

### 4.3. Shipment

![extra fee19](https://i.imgur.com/xVnq215.png)

### 4.4. Credit Memo

![extra fee20](https://i.imgur.com/n1tI2M8.png)


## 5. Email
### 5.1. Order Email

![extra fee21](https://i.imgur.com/t6U8Xk5.png)

### 5.2. Invoice Email

![extra fee22](https://i.imgur.com/OKoJybq.png)

### 5.3. Shipment Email

![extra fee23](https://i.imgur.com/BIoFaDD.png)

### 5.4. Credit Memo Email

![extra fee24](https://i.imgur.com/cOAWqHP.png)

  
## 6. Compatible with Mageplaza One Step Checkout

![extra fee25](https://i.imgur.com/T7BHIPC.png)

## 7. Compatible with Mageplaza PDF Invoice

### 7.1. PDF Order

![extra fee26](https://i.imgur.com/j9qvd2k.png)

### 7.2. PDF Invoice

![extra fee27](https://i.imgur.com/blztfLE.png)

### 7.3. PDF Shipment

![extra fee28](https://i.imgur.com/huKzDyo.png)

### 7.4. PDF Credit Memo

![extra fee29](https://i.imgur.com/xFp6eFX.png)

## 8. Compatible with PDF of Magento
### 8.1. PDF Invoice

![extra fee30](https://i.imgur.com/YqPkCUw.png)

### 8.2. PDF Shipment

![extra fee31](https://i.imgur.com/0SfCytC.png)

### 8.3. PDF Credit Memo

![extra fee32](https://i.imgur.com/tJIdwQj.png)

## 9. How to custom using the layout handle

- To display Extra Fee in Magento's default email, you need to visit `Marketing > Communications > Email Templates`. You can create a new template for order, invoice, shipment, credit memo, etc. Use different code for each template to display Extra Fee data (do the same for PDF Invoice templates). Note: If there is extra fee data, this data will be displayed and vice versa, if there is no data, this template will be the same as normal Magento template.
  - **Order, Shipment**
    - Get Extra Fee information at Payment Method.
```    
    {{if order.getHasBillingExtraFee()}}
				 {{layout handle="mp_billing_extra_fee" order=$order area="frontend" item=$order}}
			 {{/if}}
```

   - Get Extra Fee information at Shipping Method.
   
```
{{if order.getHasShippingExtraFee()}}
				 {{layout handle="mp_shipping_extra_fee" order=$order area="frontend" item=$order}}
			 {{/if}}
```

  - Get Extra Fee information at Cart Summary. Note: The rules with `Apply Type = Automatic` will also appear in Cart Summary in the backend and display on the template.

```
{{if order.getHasExtraFee()}}
                                 <h3>{{trans "Extra Fee"}}</h3>
				 {{layout handle="mp_extra_fee" order=$order area="frontend" item=$order}}
			 {{/if}}
```

  - **Invoice**
    - Get Extra Fee information at Payment Method:
    
```
{{if invoice.getHasBillingExtraFee()}}
				<h3>{{trans "Payment ExtraFee"}}</h3>
				 {{layout handle="mp_billing_extra_fee" order=$order area="frontend" item=$invoice}}
			 {{/if}}
```

  - Get Extra Fee information at Shipping Method
  
```
{{if invoice.getHasShippingExtraFee()}}
				 {{layout handle="mp_shipping_extra_fee" order=$order area="frontend" item=$invoice}}
			 {{/if}}
```

  - Get Extra Fee information at Cart Summary. Note: The rules with `Apply Type = Automatic` will also appear in Cart Summary in the backend and display on the template.
  
```
{{if invoice.getHasExtraFee()}}
				<h3>{{trans "Extra Fee"}}</h3>
				 {{layout handle="mp_extra_fee" order=$order area="frontend" item=$invoice}}
			 {{/if}}
```

  - **Credit Memo**:
    - Get Extra Fee information at Payment Method
    
```
{{if creditmemo.getHasBillingExtraFee()}}
				 {{layout handle="mp_billing_extra_fee" order=$order area="frontend" item=$creditmemo}}
			 {{/if}}
```

  - Get Extra Fee informaiton at Shipping Method
  
```
{if creditmemo.getHasShippingExtraFee()}}
				 {{layout handle="mp_shipping_extra_fee" order=$order area="frontend" item=$creditmemo}}
			 {{/if}}
```

  - Get Extra Fee information at Cart Summary. Note: The rules with `Apply Type = Automatic` will also appear in Cart Summary in the backend and display on the template.

```
{{if creditmemo.getHasExtraFee()}}
				<h3>{{trans "Extra Fee"}}</h3>
				 {{layout handle="mp_extra_fee" order=$order area="frontend" item=$creditmemo}}
			 {{/if}}
```



``Note``: 
- You can view the template of PDF Order when it is compatible with Extra Fee extension [here](https://github.com/mageplaza/pdf-invoice-templates/blob/master/invoice/pdf-invoice-extra-fee.html)
- For Invoice and Credit Memo, all fees of Extra Fee will be added to Invoice or Credit Memo first.




