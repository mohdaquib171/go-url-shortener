# URL Shortener in Go

This project is a basic URL shortener built using Go. It converts long URLs into short, shareable links and redirects users to the original URLs.

## Features

- Shorten long URLs into shorter links.

- Redirect users from the short link to the original URL.

- Server listens on port 3000 by default, with an option to change the port in the code.

## Prerequisites

- [Go](https://golang.org/doc/install) installed on your system.

- Basic understanding of Go and Git.

## Getting Started

### 1. Clone the Repository

Start by cloning the repository to your local machine:

```sh
git clone https://github.com/mohdaquib171/go-url-shortener.git
cd go-url-shortener
```

### 2. Run the Server

Navigate to the project directory and launch the server with:

```sh
go run main.go
```

By default, the server listens on port `3000`. You can change this port in the `main.go` file if needed.

## How to Use

### Shorten a URL

To shorten a URL, send a POST request to the `/shorten` endpoint with the URL you want to shorten. Here’s an example using `curl`:

```sh
curl -X POST http://localhost:3000/shorten -H "Content-Type: application/json" -d '{"url": "https://example.com"}'
```

The service will respond with a shortened URL.

### Access the Original URL

To visit the original URL, use the shortened link in your browser or send a GET request to the `/redirect/{id}` endpoint, where `{id}` is the unique identifier for your short URL:

```sh
curl http://localhost:3000/redirect/abcdef
```

This will redirect you to the original link.

## Demo

![Demo](demo.gif)
---
