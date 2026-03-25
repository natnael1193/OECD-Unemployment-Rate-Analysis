# Data Instructions

## Large Data Files

The large CSV files (data.csv and oecd_data.csv) are not included in this repository due to GitHub's file size limitations (100MB limit).

## How to Get the Data

### Option 1: Download from Original Source
1. Visit the OECD Employment Database
2. Select the relevant employment and unemployment statistics
3. Download the data for your countries/regions of interest
4. Place the files in the `data/` directory

### Option 2: Sample Data
If you need sample data for testing, you can:
1. Use the first 1000 rows of the original dataset
2. Create a smaller subset with key countries and time periods

### Option 3: Git LFS (Large File Storage)
If you have Git LFS set up:
```bash
git lfs track "data/*.csv"
git add .gitattributes
git commit -m "Track CSV files with LFS"
```

## Data Structure

The expected data files should have these columns:
- `structure`, `strucuture_id`, `structure_name`
- `action`, `ref_area`, `reference_area`
- `measure`, `measures`, `unit_measure`, `unit_of_measure`
- `sex`, `sexes`, `age`, `ages`
- `labour_force_status`, `labour_force_statuses`
- `time_period`, `time_periods`
- `obs_value`, `obs_values`, `obs_status`, `obs_statuses`
- `unit_multiplier`, `unit_multipliers`, `decimal`, `decimals`

## Notebook Usage

When running the notebooks, ensure:
1. Data files are placed in the `data/` directory
2. File names match: `data/data.csv` and `data/oecd_data.csv`
3. Data has the expected column structure

## File Sizes Reference
- `data.csv`: ~160MB (original)
- `oecd_data.csv`: ~112MB (original)

If you encounter memory issues, consider:
- Using a subset of the data
- Processing in chunks
- Using pandas with `chunksize` parameter
