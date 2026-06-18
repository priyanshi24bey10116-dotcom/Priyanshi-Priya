# Final Project Readme
# Personal Knowledge Base (Second Brain)

## Project Overview

Personal Knowledge Base (Second Brain) is a backend REST API application developed using Node.js, Express.js, MongoDB, and Mongoose. The system allows users to store, organize, categorize, search, and retrieve knowledge in a centralized repository.

The application serves as a digital memory system where users can save notes, learning resources, project information, research content, and important references for future access.

---

## Objectives

* Build a centralized knowledge management system.
* Store and manage notes using MongoDB.
* Organize information using Categories and Tags.
* Implement CRUD operations through REST APIs.
* Enable quick retrieval through Search functionality.
* Demonstrate MongoDB relationships and data modeling.
* Generate analytics using MongoDB aggregation concepts.
* Provide API documentation using Swagger UI.

---

## Technology Stack

### Backend

* Node.js
* Express.js

### Database

* MongoDB
* MongoDB Compass
* Mongoose ODM

### API Testing

* Postman

### Documentation

* Swagger UI
* Swagger JSDoc

### Version Control

* Git
* GitHub

---

## Project Architecture

```text
Client (Postman / Swagger)

        |

        V

Express Routes

        |

        V

Controllers

        |

        V

Mongoose Models

        |

        V

MongoDB Database
```

---

## Database Collections

### Notes Collection

Stores user knowledge and notes.

Fields:

* title
* content
* category
* tags
* isFavorite
* createdAt
* updatedAt

### Categories Collection

Stores note categories.

Fields:

* name
* description

### Tags Collection

Stores reusable tags.

Fields:

* name

---

## MongoDB Relationships

### One-to-Many

Category → Notes

Example:

Programming

* MongoDB Notes
* Express Notes
* NodeJS Notes

### Many-to-One

Many Notes belong to a single Category.

### Many-to-Many

Notes ↔ Tags

Example:

Tag: MongoDB

* Note 1
* Note 2
* Note 3

A note can contain multiple tags and a tag can be associated with multiple notes.

---

## Features Implemented

### Notes Management

* Create Note
* Get All Notes
* Get Note By ID
* Update Note
* Delete Note

### Category Management

* Create Category
* Get Categories

### Tag Management

* Create Tag
* Get Tags

### Search Functionality

Search notes using keywords present in:

* Title
* Content

### Favorite Notes

* Mark notes as favorite
* Retrieve favorite notes

### Category Filtering

Retrieve notes based on category.

### Tag Filtering

Retrieve notes based on tags.

### Recent Notes

Retrieve recently added notes.

### Dashboard Analytics

Provides:

* Total Notes
* Total Categories
* Total Tags
* Favorite Notes Count
* Recent Notes

### Swagger Documentation

Interactive API documentation and testing interface.

---

## REST API Endpoints

### Notes

```http
POST   /api/notes
GET    /api/notes
GET    /api/notes/:id
PUT    /api/notes/:id
DELETE /api/notes/:id
```

### Search

```http
GET /api/notes/search
```

### Favorites

```http
PATCH /api/notes/:id/favorite
GET   /api/notes/favorites
```

### Category Filter

```http
GET /api/notes/category/:categoryId
```

### Tag Filter

```http
GET /api/notes/tag/:tagId
```

### Recent Notes

```http
GET /api/notes/recent
```

### Categories

```http
POST /api/categories
GET  /api/categories
```

### Tags

```http
POST /api/tags
GET  /api/tags
```

### Dashboard

```http
GET /api/dashboard
```

---

## Seed Data

The project includes:

### Categories

* 15 Categories

### Tags

* 15 Tags

### Notes

* 50 Notes

Generated using:

```bash
node seed.js
node seedNotes.js
```

---

## Installation

### Clone Repository

```bash
git clone <repository-url>
```

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Create a .env file:

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/secondbrain
```

### Run Application

```bash
npm run dev
```

---

## API Documentation

Swagger UI:

```text
http://localhost:5000/api-docs
```

---

## Testing

The APIs were tested using:

* Postman
* Swagger UI

MongoDB operations were verified through:

* MongoDB Compass
* MongoDB Shell (mongosh)

---

## Results

The system successfully provides:

* Knowledge storage
* Knowledge organization
* Search and retrieval
* Categorization
* Tagging
* Analytics generation
* MongoDB relationship implementation
* REST API-based access

---

## Future Scope

* User Authentication using JWT
* User-specific Notes
* Pagination
* Sorting
* File Attachments
* AI-powered Note Summarization
* Semantic Search
* Recommendation System
* Cloud Deployment

---

## Author

Rudraksh Mishra

B.Tech CSE

Personal Knowledge Base (Second Brain) Project
