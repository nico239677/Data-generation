# Data-generation
The objective is to generate fake data of daily sales/orders, for different retailers selling similar products, with <b>stories</b> that explain variations in the number of sales (eg day of the week, holiday period, marketing expenses etc).
<br><br><br>
First I create fake data, with X sales every day of the year. 
<br>
Then I add noise and constraints, so that the daily sales follow a trend that is dependent on several factors (see stories below).
<br><br><br>
This fake data makes it possible:
<br>
1/ with Time Series to predict the number of sales in the future
<br>
2/ to try to <b>explain</b> the variation in sales with the stories

# Files
<b>Generating data - Table generator vf.py</b>: contains the code to generate fake data --> can be used to generate fake data, with the possibility to modify parameters, 
add or remove stories...
<b>data_retailers_random_weekly_coeffs.csv</b>: contains the fake generated data for 100 retailers
<b>retailer_config_file_random_weekly_coeffs.txt</b>: contains the generated parameters for each of the 100 retailers

Using the generated data to generate predictions:
- With time Series: <b>Generating data - Executing Models on Time Series.ipynb</b> --> to predict the number of orders on the next days, with RNN/LSTM
- With static data: <b>Generating data - Executing Models on Static Data.ipynb</b> --> preprocessing to convert the table containing the fake data on all retailers
into static data, before applying RNN
