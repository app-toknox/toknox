# TokNox
### TokNox repository for Algorand Hackathon 2024 Change The Game.

TokNox is a Tokenization platform built on the Algorand blockchain to notarize, manage, store, and sign every digital file. By revolutionizing the way users interact with blockchain technology and offering a simple, secure, and transparent platform for tokenization, Toknox opens the door to blockchain for everyone. While ensuring all digital files and transactions are managed safely, with its intuitive interface, it empowers users to leverage blockchain's potential without needing to understand its complexities, making digital asset management effortless and efficient.

Here is a comprehensive documentation guide for the app: https://docs.toknox.com/

### Here's how to get your development environment set up and running for both the front-end and back-end components of this application.

# TokNox - Back-End

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Local Usage](#local-usage)
  - [Application](#application)
  - [Database](#database)
- [Documentation](#documentation)

## Getting Started

To get started, follow the steps below.

### Prerequisites

Before you begin, make sure you have the following software installed:

- [_Docker_](https://docs.docker.com/get-docker/)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/blockchain-italia/toknox-be.git

2. Navigate to the project directory:

   ```bash
   cd toknox-be
   
3. Run the containers:

   ```bash
   docker compose -f ./docker/docker-compose-dev.yml up -d
   
4. Enter inside the container:

   ```bash
   docker compose -f ./docker/docker-compose-dev.yml exec app sh
   
5. Enter inside the virtual environment:

   ```bash
   source $(poetry env info --path)/bin/activate
   
6. **[OPTIONAL]** If you already have a database, set its revision:

    ```bash
    flask db stamp head

7. Apply the migration:

    ```bash
    flask db upgrade

## Local Usage

### Application

Once the project is set up, you can start using the application navigating to [http://localhost:5050](http://localhost:5000).

### Database

If the database schema has changed, you will need to create a new migration and apply it.

1. Enter inside the container:

   ```bash
   docker compose -f ./docker/docker-compose-dev.yml exec app sh

2. Enter inside the virtual environment:

   ```bash
   source $(poetry env info --path)/bin/activate

3. Create a migration:

   ```bash
   flask db migrate -m "<migration-message>"

4. Apply the migration:

   ```bash
   flask db upgrade
   
## Documentation

The API documentation is available at [http://localhost:5050/docs](http://localhost:5000/docs).



# Toknox Frontend

This is a [Toknox](https://toknox.com//) frontend project bootstrapped with `create-t3-app`.
This project use [Next.js](https://nextjs.org) as framework.


## Learn More

To learn more about the [T3 Stack](https://create.t3.gg/), take a look at the following resources:

- [Documentation](https://create.t3.gg/)
- [Learn the T3 Stack](https://create.t3.gg/en/faq#what-learning-resources-are-currently-available) — Check out these awesome tutorials

You can check out the [create-t3-app GitHub repository](https://github.com/t3-oss/create-t3-app) — your feedback and contributions are welcome!


## How to start

### Prerequisites

Before you begin, make sure you have the following software installed on your machine:

- Node.js
- PNPM (You can install it globally using `npm install -g pnpm`)

### Installation

1. Clone the repository:

   ```bash
    git clone https://github.com/blockchain-italia/toknox-fe.git
   ``` 
2. Enter into folder:

    ```bash
    cd toknox-fe
   ``` 
3. Install dependencies:

    ```bash
    pnpm install
   ``` 
4. Create an .env file with this params:

    ```bash
    NEXT_PUBLIC_NETWORK=""
    NEXT_PUBLIC_API_URL=""
   ``` 




### Development

To start the development server, run:
```bash
   pnpm run dev
   ``` 
This will start the Next.js development server, and you can access the application at http://localhost:3000.   
