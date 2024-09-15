# Cheat Sheet: Importing Data Sets

## Read CSV data set

- Read the CSV file containing a data set to a pandas data frame

```
df = pd.read_csv(<CSV_path>, header = None) 
# load without header 
df = pd.read_csv(<CSV_path>, header = 0) 
# load using first row as header
```

## Print first few entries
- Print the first few entries (default 5) of the pandas data frame

```
df.head(n) #n=number of entries; 
```

## Print last few entries	
- Print the last few entries (default 5) of the pandas data frame	
```
df.tail(n) #n=number of entries
```

## Assign header names	
- Assign appropriate header names to the data frame	

```
df.columns = headers
```

## Replace "?" with NaN	
- Replace the entries "?" with NaN entry from Numpy library	
```
df = df.replace("?", np.nan)
```

## Retrieve data types	
- Retrieve the data types of the data frame columns	
```
df.dtypes
```

## Retrieve statistical description	
Retrieve the statistical description of the data set. Defaults use is for only numerical data types. Use include="all" to create summary for all variables	

```
df.describe() #default use df.describe(include="all")
```

## Retrieve data set summary	
- Retrieve the summary of the data set being used, from the data frame	

```
df.info()
```

## Save data frame to CSV	
- Save the processed data frame to a CSV file with a specified path	

```
df.to_csv(<output CSV path>)
```
