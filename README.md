## Blockchain using Go

This program implements a simple blockchain in Go. Each block in the blockchain contains a timestamp, data, and the hash of the previous block. The data in each block is represented as an integer (in this case, the heart rate).

The program includes a `main` function that creates a genesis block and then append it to the blockchain. It also contains a `run` function that starts a HTTP server and listens for incoming requests.

There are two API endpoints:

* `GET /`: Returns the entire blockchain
* `POST /`: Creates a new block in the blockchain

To test the program, you can use `curl` to send requests to the API endpoints. For example, you can use the following command to get the blockchain:

```
curl -X GET http://localhost:8888/
```

You can use the following command to create a new block in the blockchain:

```
curl -X POST -H "Content-Type: application/json" -d '{"BPM":60}' http://localhost:8888/
```
