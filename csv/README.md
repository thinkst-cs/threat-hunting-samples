Parquet Files Converted to CSV

```from pathlib import Path
import pandas as pd

data_dir = Path('dataset-2/complete')
full_df = pd.concat(
    pd.read_parquet(parquet_file)
    for parquet_file in data_dir.glob('*.parquet')
)
full_df.to_csv('dataset-2-csv_file.csv')
```

### Copy all files into one folder, then run the python snippet.

`cp **/*.parquet ./complete`
