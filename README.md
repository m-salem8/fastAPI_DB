# FastAPI Exam Question Database

This is a documentation guide for the FastAPI application that serves as an exam question database. The application allows users to retrieve exam questions based on specific criteria, and admin users with special credentials can add new questions to the database.

## Table of Contents

- [Introduction](#introduction)
- [API Endpoints](#api-endpoints)
  - [Health Check](#health-check)
  - [Retrieve Exam Questions](#retrieve-exam-questions)
  - [Add New Question (Admin)](#add-new-question-admin)
- [Authentication and Authorization](#authentication-and-authorization)
- [Architecture Choices](#architecture-choices)
- [Installation](#installation)
- [Usage](#usage)
- [Conclusion](#conclusion)

## Introduction

This FastAPI application serves as an exam question database where users can retrieve exam questions based on specific criteria. The application also includes authentication and authorization mechanisms to ensure secure access to the endpoints.

## API Endpoints

### Health Check

Endpoint: `/health`

This endpoint allows users to check the health of the API. It returns a simple message confirming that the API is up and running.

### Retrieve Exam Questions

Endpoint: `/test/{type}/{subject}/{q_num}`

This endpoint retrieves exam questions based on the provided criteria: question type, subject, and the number of questions (5, 10, or 20). Users need to provide basic authentication to access this endpoint. Invalid inputs are handled with appropriate error responses.

### Add New Question (Admin)

Endpoint: `/update`

This endpoint allows admin users with special credentials to add new questions to the database. It requires authentication as an admin user. Users can submit a new question using a PUT request with a JSON body containing question details.

## Authentication and Authorization

The application uses basic authentication to verify user credentials. Users need to provide their username and password in the `Authorization` header. Admin users with the username "admin" and password "4dm1N" are authorized to add new questions.

## Architecture Choices

The application is built using FastAPI, a modern web framework for building APIs with Python. It uses an Excel spreadsheet as the data source for exam questions. The code is organized into different modules for improved readability and maintainability.

## Installation

To install the required dependencies, create a `requirements.txt` file with the following content:
