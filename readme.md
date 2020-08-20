# Glossary
    ['Date', 'Close', 'Change', 'Pct_Change', 'Volume', 'Org_Volume', 'Foreign_Volume', 'Foreign_Count', 
    'Foreign_Pct', 'DJI_Close', 'IR', 'USD_Bar', 'XR', 'XR_Pct_Change']

    Date : Date in yy/mm/dd format
    Close : Closing price of the stock
    Change : Change in price of the stock relative to previous closing price
    Pct_Change : Percentage change of Change
    Volume : Volume of stocks traded
    Org_Volume : Volume of stocks traded by organizations and corporates
    Foreign_Volume : Volume of stocks traded by foreign investors
    Foreign_Count : Number of stocks possessed by foreign investors
    Foreign_Pct : Percentage of total stock possessed by foreign investors
    DJI_Close : Dow Jones Index closing value
    IR : Interest rate in South Korea
    USD_Bar : USD per barrel oil (WTI)
    XR : USD to KRW exchange rate
    XR_Pct_Change : Percentage change in XR relative to previous date

    Stock data is not available during weekends and holidays. Therefore, the values for weekends and 
    holidays had been forward filled, and therefore carry the same value as the nearest last valid value. 

# Motivation
    In the recent months, I made over 50% returns by trading stocks. Therefore, I wanted to apply my 
    ad-hoc logic to a systematic/reproducible system, hence this project.

# Method
    The stock data for SK Innovation (096770) was scraped using BeautifulSoup from Naver Finance. The data
    had headers in Korean, which was translated appropriately and the respective words are explained in the
    Glossary above. Other data such as the Dow Jones Index, South Korean Interest Rates, WTI Oil Prices, 
    USD/KRW, and Exhcange Rates were all found online from their respective websites. 

    All data had different formats and shapes, so data was preprocessed in the Data_Preprocessing part, 
    and the processed data was explored, and a model was trained in the EDA_Model part. 

# Result
    Amongst many regression models, the Random Forest Regressor produced the lowest RMSE value, 
    and by tuning the parameters through GridSearchCV, the final RMSE was the lowest acheived 
    amongst all methods/parameters with 3493.680056730698.
