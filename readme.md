# Ref Markdown CSV Example Template

This project is an example template that demonstrates how to create a simple HTML dashboard page which:

- Displays content from a markdown file (`data-reference.md`)
- Shows a preview of data from a CSV file (`data.csv`)
- Can be hosted on Amazon S3 and linked from a dashboard

## Project Structure

- **data-reference.html**  
  An HTML file that uses [marked](https://github.com/markedjs/marked) to render markdown content from `data-reference.md`.
  
- **data-reference2.html**  
  An alternative version of the HTML file that includes interactive CSV preview features, such as column sorting and a preview table (first 5 rows).

- **data-reference3.html**  
  A modern, minimalist HTML version with improved styling and CSV preview, ready for integration as part of a dashboard view.

- **data-reference.md**  
  A markdown file containing the dashboard description, details about the data, and download link for the CSV file.

- **data.csv**  
  A sample CSV file with fake data for regions, product categories, sales amounts, and transaction dates.

- **readme.md**  
  This file, which provides an overview of the project.

## Usage

You can open any of the HTML files in your browser to preview the dashboard example. For dynamic markdown rendering and CSV preview, ensure the HTML files and the accompanying CSV and markdown files are served from a web server or a static hosting service like Amazon S3.

## Hosting on S3

To host these files on [Amazon S3](https://aws.amazon.com/s3/):

1. Create an S3 bucket and upload all project files.
2. Configure the bucket for static website hosting.
3. Set permissions to allow public read access as needed.
4. Link to `data-reference.html`, `data-reference2.html`, or `data-reference3.html` from your dashboard, depending on your preferred layout and functionality.

## Example Dashboard Link

Once the files are hosted on S3, you can link them from your dashboard. For example:

```html
<a href="https://your-bucket.s3.amazonaws.com/data-reference.html" target="_blank">Dashboard Data Reference</a>