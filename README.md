## Exploratory Data Analysis

CORRELATION WITH SALES PRICE

SalePrice Probablity Density Function

![dist_image](https://user-images.githubusercontent.com/109108274/183962915-d580530c-66ca-48df-a749-b9d208466996.png)

Histogram of diffrent Features

![Hist_1](https://user-images.githubusercontent.com/109108274/183964506-7fec3d63-de41-4149-99a9-e38b7a411aa3.png)

Scatter Plot of Every Feature with SalePrice

![Scat_1](https://user-images.githubusercontent.com/109108274/183965926-a20c6c33-5afc-4366-9478-9619ad546cbd.png)
![Scat_2](https://user-images.githubusercontent.com/109108274/183965985-3af7f13b-7624-4984-b5c1-58274e011975.png)
![Scat_3](https://user-images.githubusercontent.com/109108274/183965989-abb64e21-ca37-4791-96de-49f578b190eb.png)
![Scat_4](https://user-images.githubusercontent.com/109108274/183965991-cd391472-c9b4-4d7c-b460-679c5d7338a6.png)
![Scat_5](https://user-images.githubusercontent.com/109108274/183965997-f8c07408-e4df-489c-94ac-7e2ae6ffacde.png)
![Scat_6](https://user-images.githubusercontent.com/109108274/183966000-a7c94e21-b835-42f1-8c97-3527938758c6.png)
![Scat_7](https://user-images.githubusercontent.com/109108274/183966004-291e19bd-0046-458a-849c-57ce7f88b79c.png)

Strongly Coreelated Features with SalePrices

   KitchenAbvGr: -0.1392006921778576
       HalfBath: -0.08439171127179902
     MSSubClass: -0.08428413512659509
    OverallCond: -0.07785589404867797
         YrSold: -0.028922585168736813
   BsmtHalfBath: -0.02883456718548182
       PoolArea: -0.014091521506356765
   BsmtFullBath: 0.011439163340408606
         MoSold: 0.046432245223819446
      3SsnPorch: 0.06393243256889088
    OpenPorchSF: 0.08645298857147718
        MiscVal: 0.08896338917298921
     Fireplaces: 0.12166058421363891
      BsmtUnfSF: 0.16926100049514173
   BedroomAbvGr: 0.18093669310848806
     WoodDeckSF: 0.1937060123752066
     BsmtFinSF2: 0.19895609430836594
  EnclosedPorch: 0.24127883630117497
    ScreenPorch: 0.2554300795487841
        LotArea: 0.2638433538714051
   LowQualFinSF: 0.30007501655501323
     BsmtFinSF1: 0.47169042652357296
   YearRemodAdd: 0.5071009671113866
      YearBuilt: 0.5228973328794967
   TotRmsAbvGrd: 0.5337231555820284
       FullBath: 0.5745626737760822
       1stFlrSF: 0.6058521846919153
     GarageArea: 0.6084052829168346
    TotalBsmtSF: 0.6096808188074374
     GarageCars: 0.6370954062078923
       2ndFlrSF: 0.6733048324568376
      GrLivArea: 0.7086244776126515
    OverallQual: 0.7909816005838053

CONCLUSION

There is 11 strongly correlated values with SalePrice:
['YearRemodAdd', 'YearBuilt', 'TotRmsAbvGrd', 'FullBath', '1stFlrSF', 'GarageArea', 'TotalBsmtSF', 'GarageCars', '2ndFlrSF', 'GrLivArea', 'OverallQual']

FEATURE TO FEATURE RELATION

![corr](https://user-images.githubusercontent.com/109108274/183973903-dfb96291-38c2-4908-89c2-2489e8010763.png)

A lot of features seems to be correlated between each other but some of them such as YearBuild/GarageYrBlt may just indicate a price inflation over the years. As for 1stFlrSF/TotalBsmtSF, it is normal that the more the 1st floor is large (considering many houses have only 1 floor), the more the total basement will be large.

Now for the ones which are less obvious we can see that:

    There is a strong negative correlation between BsmtUnfSF (Unfinished square feet of basement area) and BsmtFinSF2 (Type 2 finished square feet). There is definition of unfinished square feet here but as for a house of "Type 2", I can't tell what it really is.
    
    HalfBath/2ndFlrSF is interesting and may indicate that people gives an importance of not having to rush downstairs in case of urgently having to go to the bathroom.
    
CONCLUSION

We can conclude that, by essence, some of those features may be combined between each other in order to reduce the number of features (1stFlrSF/ TotalBsmtSF, GarageCars/GarageArea) and others indicates that people expect multiples features to be packaged together.

QUANTATIVE TO QUANTITATIVE RELATIONSHIP

![reg1](https://user-images.githubusercontent.com/109108274/183979730-ab9c4524-f2fc-4470-8c47-7619d027ac6c.png)

CONCLUSION 

We can see that features such as TotalBsmtSF, 1stFlrSF, GrLivArea have a huge Spread. This shows that the as the SalePrice increases, Total Basement Area, 1st floor area size increases too and in a same as all these feature have approximately 1 as correlation between them.

CATEGORICAL TO QUANTITATIVE RELATIONSHIP

There is 39 non numerical features including:
['MSZoning', 'Street', 'LotShape', 'LandContour', 'Utilities', 'LotConfig', 'LandSlope', 'Neighborhood', 'Condition1', 'Condition2', 'BldgType', 'HouseStyle', 'RoofStyle', 'RoofMatl', 'Exterior1st', 'Exterior2nd', 'MasVnrType', 'ExterQual', 'ExterCond', 'Foundation', 'BsmtQual', 'BsmtCond', 'BsmtExposure', 'BsmtFinType1', 'BsmtFinType2', 'Heating', 'HeatingQC', 'CentralAir', 'Electrical', 'KitchenQual', 'Functional', 'GarageType', 'GarageYrBlt', 'GarageFinish', 'GarageQual', 'GarageCond', 'PavedDrive', 'SaleType', 'SaleCondition']

Box Plot of Basement Exposure to SalePrice to find outlier

![box1](https://user-images.githubusercontent.com/109108274/183981351-210aa079-a3c9-4f24-9e53-564875173b0b.png)

Box Plot of Sale Condition to SalePrice to find outlier

![box2](https://user-images.githubusercontent.com/109108274/183981356-cc806f27-d0b7-4b48-8052-57211f2d8e30.png)

Count Plot of Features

![Count](https://user-images.githubusercontent.com/109108274/183983127-4ed340a6-b427-4d51-ba58-58931cde85c0.png)

CONCLUSION 

We can see that some categories are predominant for some features such as Utilities, Heating, GarageCond, Functional... These features may not be relevant for our predictive model
