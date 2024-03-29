# ★ Retail Analytics Bootcamp Project

#### 1. Objective
      ⇉ The goal of this project is to **Predict The Sales** of a Retail outlet based on the historical data provided for sales.


#### 2. Column Description

      ⇉ **Item Identifier**: A code provided for the item of sale <br>
      ⇉ **Item Weight**: Weight of item <br>
      ⇉ **Item Fat Content**: A categorical column of how much fat is present in the item : ‘Low Fat’, ‘Regular’, ‘low fat’, ‘LF’, ‘reg’ <br>
      ⇉ **Item Visibility**: Numeric value for how visible the item is  <br> 
      ⇉ **Item Type**: What category does the item belong to: ‘Dairy’, ‘Soft Drinks’, ‘Meat’, ‘Fruits and Vegetables’, ‘Household’, ‘Baking Goods’, ‘Snack Foods’, ‘Frozen Foods’, ‘Breakfast’, ’Health and Hygiene’, ‘Hard Drinks’, ‘Canned’, ‘Breads’, ‘Starchy Foods’, ‘Others’, ‘Seafood’. <br>
      ⇉ **Item MRP**: The MRP price of item <br>
      ⇉ **Outlet Identifier**: Which outlet was the item sold. This will be categorical column <br>
      ⇉ **Outlet Establishment Year**: Which year was the outlet established <br>
      ⇉ **Outlet Size**: A categorical column to explain size of outlet: ‘Medium’, ‘High’, ‘Small’.  <br> 
      ⇉ **Outlet Location Type**: A categorical column to describe the location of the outlet: ‘Tier 1’, ‘Tier 2’, ‘Tier 3’  <br>
      ⇉ **Outlet Type** : Categorical column for type of outlet: ‘Supermarket Type1’, ‘Supermarket Type2’, ‘Supermarket Type3’, ‘Grocery Store’  <br>
      ⇉ **Item Outlet Sales**: The amount of sales for an item.  <br> 
      ⇉ **Source**: Whether the data is from train or test.  <br>
   
   
#### ◉ Some Important Observations from the Training dataset:

      ➥ Train Dataset have missing data values for the columns **"Item_Weight"** and **"Outlet_Size"** each of them having **1463** and **2410** missing values.

         ⇉ Item_Identifier has a high cardinality: **1559 distinct values**<br>
         ⇉ Item_Visibility has **526 / 6.2% zeros**<br>
         ⇉ Item_Weight has **17.2% missing values**<br>
         ⇉ Outlet_Size has **28.3% missing values**
   
   
#### ◉ Some Important Observations from the Testing dataset:

      ➥ Test Dataset have missing data values for the columns **"Item_Weight"** and **"Outlet_Size"** each of them having **976** and **1606** missing values.

         ⇉ Item_Identifier has a high cardinality: **1543 distinct values**<br>
         ⇉ Item_Visibility has **353 / 6.2% zeros**<br>
         ⇉ Item_Weight has **17.2% missing values**<br>
         ⇉ Outlet_Size has **28.3% missing values**
   
#### 3. Insights
      ⇉ There is no significant correlation between the variables.
      ⇉ There is moderate correlation between Item_Outlet_Sales and Item_MRP.
      ⇉ Most of the sales amount are happening for Starchy Foods or Seafood.
      ⇉ Fruits and Vegetables are the most sold items in Tier 3 and Tier 1 cities whereas Snack Foods are the most sold items in Tier 2 cities. 
      ⇉ Fruits and Vegetables are the most sold items in 3 location and Seafood is the least sold item in 3 locations.
      ⇉ Maximum sales is observed in Mid Sized Outlets
      ⇉ Most of the sales are hapenning in Supermarket Type 3.
      ⇉ There is less footfalls in outlets established in 1998 and therefore the sales is believed the least.
      ⇉ Maximum sales is observed in Tier 2 and 3 cities
      ⇉ There are no big outlets in Tier 1 cities. Hence, The sales in Tier 1 cities is low
      
      
#### 4. Linear Regression Model

#### ◉ Intuition from the Co-efficient values:

     ➥ After looking at the values of Co-efficients, we can see that
        ⇉ Each item Sales largely depends upon the Store in which we are selling it. 
        ⇉ Location of the outlet influences most of the Item Sales. 
     
#### ◉ Model Score:     
        ⇉ RMSE of the Model ⇉ 1124
        ⇉ R2 Score of the Model ⇉ 56.52


#### 5. XGBoost Regressor Model

#### ◉ Model Score:     
        ⇉ RMSE of the Model ⇉ 1115
        ⇉ R2 Score of the Model ⇉ 57.29
        
        
#### 6. XGBoost Regressor With GridSearchCV Model

#### ◉ Model Score:     
        ⇉ RMSE of the Model ⇉ 1072
        
        
#### 7. Model Evaluation
     ➥ Comparing the RMSE obtained from different models.

        ⇉ RMSE for Linear Regression - 1124
        ⇉ RMSE for XGBoost - 1115
        ⇉ RMSE for XGBoost with GridSearchCV - 1072
