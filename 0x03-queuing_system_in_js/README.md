# Queuing System in JS

## Project Overview

This project involves creating a queuing system using Node.js, Redis, and Kue. The goal is to familiarize yourself with Redis operations and Kue as a queue system. You'll learn to interact with Redis using Node.js, manage asynchronous operations, and handle job queues.

## Learning Objectives

By the end of this project, you should be able to:
- Run a Redis server and perform basic operations.
- Use a Redis client with Node.js.
- Store and manage hash values in Redis.
- Handle asynchronous operations with Redis.
- Utilize Kue for job queuing.
- Build a basic Express app interacting with Redis and Kue.

## Requirements

- Code should be compiled/interpreted on Ubuntu 18.04, Node 12.x, and Redis 5.0.7.
- All code files must use the `.js` extension and end with a newline.
- A `README.md` file must be at the root of the project directory.

## Project Setup

1. **Install Redis**
    - Download, extract, and compile Redis:
      ```bash
      $ wget http://download.redis.io/releases/redis-6.0.10.tar.gz
      $ tar xzf redis-6.0.10.tar.gz
      $ cd redis-6.0.10
      $ make
      ```
    - Start Redis and verify:
      ```bash
      $ src/redis-server &
      $ src/redis-cli ping
      ```
    - Set and get a value to test:
      ```bash
      $ src/redis-cli set Holberton School
      $ src/redis-cli get Holberton
      ```
    - Kill the Redis server:
      ```bash
      $ kill [PID_OF_Redis_Server]
      ```

2. **Install Node.js Redis Client**
    - Install `node_redis`:
      ```bash
      $ npm install redis
      ```

3. **Clone the Repository**
    - GitHub repository: [alx-backend](https://github.com/alx-backend)
    - Directory: `0x03-queuing_system_in_js`

## Tasks

1. **Redis Client**
    - Create `0-redis_client.js` to connect and log Redis client status.

2. **Basic Redis Operations**
    - Create `1-redis_op.js` to set and get values from Redis.

3. **Async Operations**
    - Create `2-redis_op_async.js` to perform async operations with Redis using `async/await`.

4. **Advanced Operations**
    - Create `4-redis_advanced_op.js` to handle hash values in Redis.

5. **Publisher and Subscriber**
    - Create `5-subscriber.js` and `5-publisher.js` to demonstrate Redis Pub/Sub.

6. **Job Creator**
    - Create `6-job_creator.js` to add jobs to the queue using Kue.

7. **Job Processor**
    - Create `6-job_processor.js` to process jobs from the queue.

8. **Track Progress and Errors**
    - Create `7-job_creator.js` to create multiple jobs and track their progress.
    - Create `7-job_processor.js` to process jobs, handle blacklisted numbers, and track progress and errors.

## Running the Project

1. **Start Redis Server**
    ```bash
    $ src/redis-server &
    ```

2. **Run Redis Client**
    ```bash
    $ npm run dev 0-redis_client.js
    ```

3. **Run Redis Operations**
    ```bash
    $ npm run dev 1-redis_op.js
    $ npm run dev 2-redis_op_async.js
    $ npm run dev 4-redis_advanced_op.js
    ```

4. **Run Publisher and Subscriber**
    - In one terminal, run the subscriber:
      ```bash
      $ npm run dev 5-subscriber.js
      ```
    - In another terminal, run the publisher:
      ```bash
      $ npm run dev 5-publisher.js
      ```

5. **Run Job Creator and Processor**
    - In one terminal, run the job creator:
      ```bash
      $ npm run dev 6-job_creator.js
      ```
    - In another terminal, run the job processor:
      ```bash
      $ npm run dev 6-job_processor.js
      ```

6. **Track Progress and Errors**
    - In one terminal, run the enhanced job creator:
      ```bash
      $ npm run dev 7-job_creator.js
      ```
    - In another terminal, run the enhanced job processor:
      ```bash
      $ npm run dev 7-job_processor.js
      ```

## Resources

- [Redis Quick Start](https://redis.io/topics/quickstart)
- [Redis Client Interface](https://github.com/NodeRedis/node-redis)
- [Redis Client for Node.js](https://github.com/NodeRedis/node-redis)
- [Kue](https://github.com/Automattic/kue) (Note: Kue is deprecated but still used in the industry)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

