

# Cutit by Organization

This Python script reads a CSV file containing data from multiple organizations and separates it into individual CSV files, one for each organization.

## Features

- Reads a single input CSV file
- Separates data based on a specified organization column
- Creates individual CSV files for each unique organization
- Preserves the original CSV structure (headers and all columns)
- Handles file and directory operations safely

## Requirements

- Python 3.x

## Usage

1. Place the `cutit.py` script in the same directory as your input CSV file.

2. Open a terminal or command prompt and navigate to the directory containing the script and your input file.

3. Run the script using Python:

   ```
   python cutit.py
   ```

4. The script will create a new directory (default name: `output_files`) and populate it with separate CSV files for each organization.

## Configuration

Before running the script, open `cutit.py` and modify the following variables at the bottom of the file:

- `input_file`: The name of your input CSV file (e.g., 'data.csv')
- `output_directory`: The name of the directory where separated files will be saved (e.g., 'separated_files')
- `organization_column`: The name of the column in your CSV that contains the organization names (e.g., 'Company')

Example:

```python
input_file = 'data.csv'
output_directory = 'separated_files'
organization_column = 'Company'
```

## Function Details

The main function `separate_csv_by_organization(input_file, output_directory, organization_column)` does the following:

1. Creates the output directory if it doesn't exist.
2. Reads the input CSV file.
3. Groups the data by organization.
4. Creates separate CSV files for each organization in the output directory.

## Error Handling

The script includes basic error handling:

- It will create the output directory if it doesn't exist.
- It will raise a `ValueError` if the specified organization column is not found in the CSV file.

## Limitations

- The script assumes that the input CSV file has a header row.
- Organization names containing forward slashes ('/') will have them replaced with underscores ('_') in the output file names.
- Very large CSV files might require additional optimization for memory efficiency.

## Contributing

Feel free to fork this repository and submit pull requests with any enhancements.

## License

This project is open source and available under the [MIT License](LICENSE).
