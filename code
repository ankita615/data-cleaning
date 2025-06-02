import pandas as pd

# Step 1: Load the dataset
df = pd.read_csv('marketing_campaign.csv', sep=';')  # use correct separator

# Step 2: Quick look at data
print(df.info())
print(df.head())

# Step 3: Handle missing values
print(df.isnull().sum())  # check nulls

# Remove rows with missing values
df.dropna(inplace=True)

# Step 4: Remove duplicates
df.drop_duplicates(inplace=True)

# Step 5: Standardize text columns
df['Education'] = df['Education'].str.lower()
df['Marital_Status'] = df['Marital_Status'].str.lower()

# Step 6: Convert date columns
df['Dt_Customer'] = pd.to_datetime(df['Dt_Customer'], format='%d-%m-%Y')

# Step 7: Rename columns
df.columns = df.columns.str.lower().str.replace(' ', '_')

# Step 8: Check and fix data types
df['income'] = df['income'].astype(int)

# Step 9: Save cleaned data
df.to_csv('cleaned_customer_personality.csv', index=False)
