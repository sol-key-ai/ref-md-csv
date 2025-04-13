# Ref Markdown CSV Example Template

This project is a template that can be used to automatically generate a reference page for an analytics dashboard, including automated data file previews, meta-data and downloads

- Displays content from a markdown file (`data-reference.md`)
- Shows a preview of sample data from CSV files
- Reads [data-files.json](./data-files.json) to automatically load the CSV files for preview and download
- Can be hosted on Amazon S3 and linked from a dashboard

## Project Structure

- [Dashboard Data Reference](./data-reference.html)  
  The main HTML file that uses [marked](https://github.com/markedjs/marked) to render markdown content from `data-reference.md`. It also includes interactive CSV preview features, such as column descriptions and a preview table (first 5 rows).

- **data-reference.md**  
  A markdown file containing the dashboard description, details about the data, and download links for the CSV files.

- **data-files.json**  
  A JSON file that contains metadata about the CSV files, including file names, descriptions, and column details.

- **Sample CSV Data**  
  - **data1.csv**: Sample CSV file with housing price data (average and median prices, number of sales).  
  - **data2.csv**: Sample CSV file with employee data (names, ages, departments).  
  - **data3.csv**: Sample CSV file with housing rental data (average and median rents, number of rentals).

- **readme.md**  
  This file, which provides an overview of the project.

## Usage

You can open [Dashboard Data Reference](./data-reference.html) in your browser to preview the dashboard example. For dynamic markdown rendering and CSV preview, ensure the HTML files and the accompanying CSV and markdown files are served from a web server or a static hosting service like Amazon S3.

## Hosting on S3

To host these files on [Amazon S3](https://aws.amazon.com/s3/):

1. Create an S3 bucket and upload all project files.
2. Configure the bucket for static website hosting.
3. Set permissions to allow public read access as needed.
4. Link to `data-reference.html` from your dashboard, depending on your preferred layout and functionality.

## Example Dashboard Link

Once the files are hosted on S3, you can link them from your dashboard. For example:

```html
<a href="https://your-bucket.s3.amazonaws.com/data-reference.html" target="_blank">Dashboard Data Reference</a>
```

## Data Files Structure

Below is an example entry from [data-files.json](./data-files.json) to illustrate its structure. This file provides metadata for each CSV file, and the page automatically loads the CSV files described here for preview and download.

```json
{
  "files": [
    {
      "fileName": "data1.csv",
      "description": "Sample CSV with housing price data.",
      "columns": [
        {
          "name": "Price",
          "description": "Average house price."
        },
        {
          "name": "Median",
          "description": "Median house price."
        }
      ]
    }
    // ...additional entries...
  ]
}
```