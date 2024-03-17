# UDP Network Writer Challenge
### Disclaimer: prior to this challenge I had next to no knowledge about golang and the intricacies involved in a UDP network.. I still don't fully get it but hey I finished the task! :D
## Introduction
This is a hiring challenge for the intern role for core media team at our company. The goal of this challenge is to write a UDP network writer that performs significantly better than the baseline implementation.

## Challenge Description
In the `benchs_test.go` file, you will find a benchmark test that measures the performance of the UDP network writer. Your task is to improve the performance of the writer so that it is at least 2 times faster than the baseline implementation.

## Getting Started
To run the benchmark test, use the following command:
```bash
go test -benchmem -bench BenchmarkConnections
```

## Submission
Changes made:
- Create a UDP connection that will be used for writing to the ports
- Allocate buffer for all messages
- Copy messages to buffer while checking for overflow
- Send messages to the respective ports

## Evaluation
The golang benchmark test logs are of the following structure:
```
BenchmarkConnections-8   	<number of iterations per second>	       <time for processing each iteration> ns/op    <bytes allocated per iteration> B/op   <number of allocations per iteration> allocs/op
```
Your solution will be evaluated based on the following criteria (in this order):
- Number of terations per second
- Time for processing each iteration
- Code quality, E.g. readability, maintainability, and performance
- Explanation of the solution and trade-offs
- Bytes allocated per iteration
- Number of allocations per iteration
