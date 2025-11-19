# React Node Cloudflare R2 Uploader

Proof of concept for uploading files from a React application to Cloudflare R2 storage using a secure Node.js backend and pre-signed URLs.

## Features

- **React:** User-friendly interface for selecting and uploading files.
- **Node.js:** REST API to generate and manage presigned URLs for secure file uploads.
- **Cloudflare R2 Integration:** Store files reliably in the cloud.
- **Security:** Credentials are never exposed to the client; presigned URLs expire after a set time.

## Requirements

- Node.js >= 16.x
- npm
- Cloudflare account with R2 access and API keys

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/itsronalds/react-node-r2cloudflare.git
   cd react-node-r2cloudflare
   ```

2. **Configure backend environment**
   Create a `.env` file inside `server/`:
   ```
   AWS_ENDPOINT=<your_r2_endpoint>
   AWS_ACCESS_KEY=<your_access_key>
   AWS_SECRET_KEY=<your_secret_key>
   ```

3. **Install dependencies**
   ```bash
   cd client
   npm install
   cd ../server
   npm install
   ```

## Running the Project

1. **Start the backend**
   ```bash
   cd server
   npm start
   ```

2. **Start the frontend**
   ```bash
   cd client
   npm start
   ```

## Usage

1. Open [http://localhost:3000](http://localhost:3000) in your browser.
2. Select a file and click "Upload".
3. The file will be uploaded to your Cloudflare R2 bucket using a temporary presigned URL.

## Security Notes

- Never expose your Cloudflare credentials in frontend code.
- Presigned URLs expire for added security.
- Limit API key permissions to only what's needed.
