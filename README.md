# Asynchronous CSV Parser with Ampt

This project showcases a simple CSV parser built using Ampt, a platform offering a high fidelity cloud environment for developing and running cloud-native applications using Node.js. The parser facilitates the uploading of CSV files through an API, processing the data, and then storing it in Ampt.

## Dependencies

- [@ampt/sdk](https://getampt.com/docs/sdk)
- [express](https://expressjs.com/)
- [@ampt/data](https://getampt.com/docs/data)
- [papaparse](https://www.papaparse.com/)
- [multer](https://github.com/expressjs/multer)

## Features

- **File Uploading**: Accepts CSV file uploads via a POST request.
- **CSV Processing**: Uses `papaparse` to parse the uploaded CSV, handling delimiters effectively.
- **Data Storage**: Employs Ampt's storage service to save parsed data.

## API Endpoints

### POST /api/csv

- Upload your CSV file to the server.
- The system will write the CSV to Ampt's storage service.
- Returns the status of the upload in a JSON format.

## Event Listeners

- **csvStorage.on("write:*.csv")**: On a `.csv` file write event, the system reads and parses the CSV file and stores the processed data.

## Setup and Usage

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```
2. **Launch Ampt CLI**:
```bash
ampt
```
3. **Install Dependencies**:

In Ampt CLI, run the following commands to install all dependencies: 

```bash
install @ampt/sdk
install express
install @ampt/data
install papaparse
install multer
```
4. **Test**:
   
Go to the URL of sandbox Ampt provides you. Upload a file, and check [Ampt Dashoard](ampt.dev) to see the file and storage.
