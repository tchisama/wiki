
### Step 1: Update Dockerfile for Development

Modify your `Dockerfile` to include the necessary development dependencies and expose the development server port. We'll use the `npm run dev` command to start the development server.

```Dockerfile
# Use official Node.js image as base
FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to work directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port that your Next.js dev server runs on
EXPOSE 3000

# Start the Next.js dev server
CMD ["npm", "run", "dev"]
```

### Step 2: Docker Compose for Development (Optional but recommended)

Using Docker Compose makes managing development environments easier. Create a `docker-compose.yml` file in the root directory of your project:

```yaml
version: '3.3'

services:
  nextjs:
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - "3000:3000"
    volumes:
      - .:/app
      - /app/node_modules
    environment:
      - NODE_ENV=development
```

### Step 3: Run Docker Compose

Open a terminal, navigate to your project directory containing the `docker-compose.yml` file, and run:

```bash
docker-compose up
```

This command will start the Next.js development server in a Docker container, with hot-reloading enabled. Any changes made to your code locally will trigger an automatic refresh in the running container.

### Notes:

- The `docker-compose.yml` file mounts your local directory as a volume inside the Docker container, so any changes you make locally are immediately reflected in the container.
- Ensure your Next.js app is properly configured for development mode (`npm run dev` should start the development server).
- The `npm run dev` script should be configured to use hot-reloading for automatic refreshes during development.
- You can customize the Docker Compose file further to include additional services like databases or other dependencies required for your development environment.
