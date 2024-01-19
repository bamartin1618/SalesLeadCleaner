# Sales Lead Preprocessing Toolkit

This toolkit is an integral part of our automated pipeline, specifically designed for preprocessing sales leads. It streamlines the process of cleaning, validating, and categorizing data extracted in earlier stages of the pipeline. The toolkit is implemented in Python and heavily utilizes Pandas DataFrames, making it efficient and robust for handling large datasets. The functionalities include metadata collection, email validation, role categorization, name cleaning, and various other data processing routines.

## Purpose

The primary goal of this toolkit is to ensure that sales leads are accurately processed and ready for further analysis and engagement. It addresses common issues in lead data such as missing information, duplicates, and invalid entries, thereby enhancing the quality and reliability of the sales pipeline.

## Features

- **Metadata Collection**: Summarize missing data or categorize leads based on specific roles.
- **Email Validation**: Validate and correct email addresses to enhance contact reliability.
- **Role Categorization**: Assign roles to leads in predefined categories using advanced text processing.
- **Name Cleaning**: Standardize first and last names for consistency and accuracy.
- **General Data Processing**: Implement routines for handling null values, duplicates, and validating lead information.

## Requirements

To utilize this toolkit effectively, you need:

- Python 3.x
- Pandas
- Regular Expressions (re module)
- email-validator
- requests

## Installation

Begin by cloning the repository to your local machine:

```bash
git clone https://github.com/bamartin1618/SalesLeadCleaner.git
cd SalesLeadCleaner
```

Install all the required Python packages:

```bash
pip install pandas email-validator requests
```

## Usage

Each function within this toolkit is designed for specific aspects of sales lead preprocessing. Here is a brief overview:

### Collect Metadata

```python
collect_metadata(df, style)
```
- `df`: DataFrame containing lead data.
- `style`: Choose "NULL" for analyzing missing data or "ROLE" for role categorization.

### Validate Email

```python
validate_email(email)
```
- `email`: Email address string of the lead to be validated.

### Bucket Roles

```python
bucket_roles(roles, count)
```
- `roles`: String list of roles associated with the leads.
- `count`: The number of roles to process.

### Process Chunk

```python
process_chunk(df)
```
- `df`: A segment of the DataFrame with lead roles to categorize.

### Clean Names

```python
clean_names(row, indicator)
```
- `row`: A dictionary representing a row in the DataFrame.
- `indicator`: Specify "first" for first name or "last" for last name cleaning.

### Process

```python
process(df, process)
```
- `df`: The DataFrame with sales leads to be processed.
- `process`: Type of processing needed - "Nulls", "Duplicates", "Validity", "Roles", or "Names".

## Contributing

We welcome contributions to enhance and expand the capabilities of this toolkit. To contribute:

1. Fork the repository.
2. Create a new branch for your feature: `git checkout -b feature-branch`.
3. Commit your changes: `git commit -am 'Add new feature'`.
4. Push to the branch: `git push origin feature-branch`.
5. Submit a pull request.

More detailed instructions can be found in the GitHub documentation on [creating a pull request](https://help.github.com/articles/creating-a-pull-request/).

## License

This project is licensed under the MIT License. See the [LICENSE.md](LICENSE.md) file for more details.

## Acknowledgments

- Thanks to all contributors who have helped in shaping this toolkit.
- Special acknowledgment to the team and individuals involved in the development and maintenance of the sales lead automation pipeline.
