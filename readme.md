# Ref Markdown CSV Example Template

This project is an example template that demonstrates how to create a simple HTML dashboard page which:

- Displays content from a markdown file (`data-reference.md`)
- Shows a preview of data from multiple CSV files
- Can be hosted on Amazon S3 and linked from a dashboard

## Project Structure

- **data-reference.html**  
  The main HTML file that uses [marked](https://github.com/markedjs/marked) to render markdown content from `data-reference.md`. It also includes interactive CSV preview features, such as column descriptions and a preview table (first 5 rows).

- **data-reference8.html**  
  An enhanced version of the HTML file with modern styling, icons for tabs, and support for multiple CSV files with descriptions.

- **data-reference.md**  
  A markdown file containing the dashboard description, details about the data, and download links for the CSV files.

- **data-files.json**  
  A JSON file that contains metadata about the CSV files, including file names, descriptions, and column details.

- **data1.csv**  
  A sample CSV file with housing price data, including average and median prices and the number of sales.

- **data2.csv**  
  A sample CSV file with employee data, including names, ages, and departments.

- **data3.csv**  
  A sample CSV file with housing rental data, including average and median rents and the number of rentals.

- **readme.md**  
  This file, which provides an overview of the project.

## Usage

You can open any of the HTML files in your browser to preview the dashboard example. For dynamic markdown rendering and CSV preview, ensure the HTML files and the accompanying CSV and markdown files are served from a web server or a static hosting service like Amazon S3.

## Hosting on S3

To host these files on [Amazon S3](https://aws.amazon.com/s3/):

1. Create an S3 bucket and upload all project files.
2. Configure the bucket for static website hosting.
3. Set permissions to allow public read access as needed.
4. Link to `data-reference.html` or `data-reference8.html` from your dashboard, depending on your preferred layout and functionality.

## Example Dashboard Link

Once the files are hosted on S3, you can link them from your dashboard. For example:

```html
<a href="https://your-bucket.s3.amazonaws.com/data-reference8.html" target="_blank">Dashboard Data Reference</a>
```