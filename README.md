# Cryptocurrencies

# Background

  Martha is a senior manager for the Advisory Services Team at Accountability Accounting, one of your most important clients. 
  Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio 
  for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a 
  report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification 
  system for this new investment.

  The data Martha will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since 
  there is no known output for what Martha is looking for, she has decided to use unsupervised learning. To group the 
  cryptocurrencies, Martha decided on a clustering algorithm. She’ll use data visualizations to share her findings with the board.
  
# Step 1: 

Preprocessing the data for PCA - Using  Pandas, preprocess the dataset in order to perform PCA 

  a. All cryptocurrencies that are not being traded were removed
  b. Drop "IsTrading" column 
  c. Removed all the rows that have at least on null value
  d. Removed all the rows that do not have coins being mined
  e. Dropped "CoinName" column
  

# Step 2: Reducing Data Dimensions Using PCA

Applied the Principal Component Analysis (PCA) algorithm, to reduce the dimensions of the X DataFrame to three principal 
components and place these dimensions in a new DataFrame.

    a. Used the PCA algorithm to reduce the dimension of the X DataFrame down to three principal components
    b. Created "pcs_df" DataFrame which has three columns, "PC 1", "PC 2", PC 3" and has the index from "crypto_df" Dataframe
   
# Step 3: Clustering Cryptocurrencies Using K-means

Using the K-means algorithm, created an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame created 
in step 2. Then run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.

    a. Used K-means algorithm to cluster the cryptocurrencies using the PCA data, where the following steps were completed:
      - Created an elbow curve using hvPlot to find the best value for K
      - Made predictions on the K clusters of the cryptocurrencies data
      - Created a new DataFrame with the same index as the "crypto_df" DataFrame and included the following columns: "Algorithm", 
        "ProofType", "TotalCoinsMined", "TotalCoinSupply", "PC 1", "PC 2", "PC 3", "CoinName", and "Class"
    
# Step 4: Visualizing Cryptocurrencies Results

Using scatter plots with Plotly Express and hvplot, visualize the distinct groups that correspond to the three principal components 
created in Deliverable 2, then create a table with all the currently tradable cryptocurrencies using the hvplot.table() function.

    a. Plotted clusters using a 3D scatter plot and each data point shows the "CoinName" and "Algorithm" on hover
    b. Created a table with tradable cryptocurrencies using "hvplot.table() function
    c. Printed the total number of tradable cryptocurrencies
    d. Created a Dataframe that contains the "clustered_df" DataFrame index, the scaled data, and the "CoinName" and "Class" columns
    e. Created a hvplot scatter plot where the X-axis is "TotalCoinsMined", and the Y-axis is "TotalCoinSupply",  the data is ordered 
       by "Class", and it shows the "CoinName" when you hover over the data point.
    
    
    
    
    
    
   
   
   
   
   
   
   
