---
title: SAP UI5 - Add a search field
description: Add a search using the SearchField element
tags: [  tutorial>beginner, topic>html5, topic>sapui5, products>sap-hana-cloud-platform ]
---
## Prerequisites  
 - **Proficiency:** Beginner 
 - **Tutorials:** This tutorial is part of a series.  The previous tutorial is part 6: [Upgrade the Detail view](sapui5-webide-upgrade-detail-view.html)

## Next Steps
 - The next tutorial in the series is Part 10: [Add an Order Activity to the form](sapui5-webide-add-order-activity.html)

## Details
### You will learn  
You will add a `<SearchField>` control to the initial page of the application. We’ll add it as a child within the pages `subHeader` aggregation which expects a `<Bar>` control.


### Time to Complete
**10 Minutes**.

---

1.  Open the `webapp/view/View1.view.xml` file, and add the following code to the `<Page>` element:

    ```xml
    <subHeader>
	```
	
	![Adding a subHeader element](1a.png)
	 
   You will also need to add an ID field to the `<List>` element, directly below.  Add this to the `<List>` element:
   
   
   ```
   id="List"
   ```
   
	![Adding an id tag to the List element](1b.png)
   
2.  Open the `webapp/view/View1.controller.js` file, and update the Controller with the following new functionality:

    >**Note** Be careful with the exact placement of this code.  The code should go after a single closed braces `}`, on line 14.
    

	```javascript
   		,
			
	```
  
	![Add the handleSearch method to the controller](2.png)
	 
3.  Run your application.  You should see the search box at the top of the list, right below the words `Product Overview`.
   
   > **NOTE**: If the search does not work, check the `View1.view.xml` file, and make sure the `<List>` element has an *id* parameter.
   
	![Search field is displayed](3.png)


## Next Steps
 - The next tutorial in the series is Part 10: [Add an Order Activity to the form](sapui5-webide-add-order-activity.html)

## Additional Information
- [`<SearchField>` element](https://sapui5.hana.ondemand.com/explored.html#/entity/sap.m.SearchField/samples)
- [Model filter](https://sapui5.hana.ondemand.com/docs/api/symbols/sap.ui.model.Filter.html)
