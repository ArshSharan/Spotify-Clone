# Spotify Clone

A full stack Spotify clone where users can upload, store, and stream audio files. This project does not use Spotify's developer APIs; instead, audio files are stored in a database and processed in the background before being fetched for playback.

## Table of Contents
- [Objective](#objective)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Running the Project](#running-the-project)
- [Project Structure](#project-structure)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## Objective

The goal of this project is to build a Spotify-like application where users can:
- Upload audio files.
- Store audio files in a database or cloud storage.
- Stream audio files from their library.
- Manage their music library, playlists, and user accounts.

## Tech Stack

### Frontend
- **Framework**: [Next.js](https://nextjs.org/)
- **Styling**: TailwindCSS or CSS-in-JS (styled-components)

### Backend
- **Server Framework**: [Node.js](https://nodejs.org/) with [Express](https://expressjs.com/)
- **Database**: [MongoDB](https://www.mongodb.com/) for storing user data, audio metadata, and file paths
- **Background Processing**: `Bull` with Redis for handling background tasks

### Storage
- **Audio Files**: Stored in the database (using GridFS) or cloud storage like AWS S3

## Features

1. **User Authentication**
   - Sign up, log in, and log out functionality
   - JWT-based authentication for secure access
   - Password hashing with bcrypt for security

2. **Audio Upload and Storage**
   - Users can upload audio files, which are stored in the database or cloud storage
   - File metadata such as title, artist, and duration is saved in the database

3. **Background Processing**
   - Audio files are processed in the background to convert them to a standard format (e.g., MP3)
   - Metadata extraction and database updates after processing

4. **Audio Streaming**
   - Users can fetch and stream audio files from their music library
   - Supports streaming with HTTP range requests for efficient playback

5. **Playlists & Music Library**
   - Users can create, update, and delete playlists
   - Organize audio files within playlists for better management

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites
- Node.js installed
- MongoDB set up locally or use [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
- Redis installed locally (for background processing with Bull)
- AWS S3 or any cloud storage (if opting for cloud-based audio storage)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/spotify-clone.git
   cd spotify-clone
