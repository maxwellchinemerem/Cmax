# Cmax
**My first repository**
# Analysed Metropolitan csv File on python
: This is where i usd a variable name "filepath" to import my csv file
## Checking in my data
: This is where i checked my data analysed them by creating a new variable name for each of the things i want to now about the file
### Summary
: Using python is cool in analyising your data and i really look forward to be corrected in my code.

filepath = "C:\\Users\\MAXWELL CHINEMEREM\\Downloads\\6ea02dcb9775d35616240c782444428f00905123\\"

data = pd.DataFrame(columns=["Crime ID","Month","Reported by","Falls within",
                             "Longitude","Latitude","Location","LSOA code",
                             "LSOA name","Crime type","Last outcome category","Context"])

for folder in os.listdir(filepath):
  for file in os.listdir(filepath + folder):
    file_df = pd.read_csv(filepath + folder + "\\" + file)
    data = pd.concat([data,file_df])
    print("Has been added",file)
    print(data.shape)
