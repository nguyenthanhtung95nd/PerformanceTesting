# Introduction
In this article, I would like to share my knowledge about Performance Testing to an application. I hope you will have fun when reading this article

# What Is Performance Testing?
  - Performance testing is Tests how an application or resource performs under a given load to see its impact.
  - Performance testing is done after functional testing.
## Performance is measured in term of

- Response time
  > `Request Time` + `Processing Time` + `Response Time` + `Network Latency`

- Throughput
  > `Number of transactions (request/response)` / `Unit of time (milliseconds/seconds)`

  > `(K)bytes (sent/received)`/ `Unit of time (milliseconds/seconds)`

- Reliability
    > `Number of errors` / `Number of requests`

- Scalability
  Base on `Response time`, `Throughput`, `Percentage of errors`
  - Vertical Scalability: By upgrading the hardware like adding more memory or additional CPUs
  - Horizontal Scalability: By adding servers to a cluster

## Performance Requirements
  Sometimes performance requirements are given by service level agreements or contracts. Other times, you must identify the performance requirements of the application before testing. Some examples of these requirements are the

  > The average/maximum response time should be ________

  > The system should be able to support __________ pages per second

  > The system should be capable of supporting at least ________ users per hour

## Performance Testing Process
  - Step 1: Design and build tests
    - You should ask yourself questions that `How many users will be browsing the page at given time?` There will help you design the tests and build them using a tool like JMeter.
  - Step 2: Prepare the test environment
    - In this step, you have to configure a test environment similar to the production environment and everything you need to run the test
  - Step 3: Run the tests
    - In this step, the first thing you need to do is validate the test script and test data to see if the work correctly. During the   execution of the test, you can monitor the server logs and the test results to see of everything is going OK!
  - Step 4: Analyze the results
    - Then, Analyze the results to identify issues that need to be addressed. That could be related to the application, the hardware, or the database. These may lead to changes to optimize database queries, increase the memory available to the application
  - Step 5: Optimize
  - Step 6: Retest
    - Then, after each change or series of changes, the test is re-executed and the results are compared to see if the changes have a positive effect. Otherwise, more changes will be made. And this process repeats until the performance requirements are met

# Introducing JMeter
- JMeter is an open source, load testing tool this is part of the Apache Software Foundation. It was designed for testing web application.
- JMeter is developed in Java, so it uses Java Thread to simulate users. You can think of Java Thread as an individual process inside of a program. A Java program can have many of these processes running at the same time. So according to the specifications of your test, JMeter creates threads to simulate users, and for each user it creates and sends requests to a server. In turn, the server receives the request the request and responses. Then, JMeter saves the response and collects all the data it needs to present reports and graphics in real time.

## Installation
You can refer document at [here](https://jmeter.apache.org/download_jmeter.cgi)

## Plugins
JMeter has a lot of feature, however, you can install plugins to extend its capabilities.
I recommend you to install at least these four plugins
  - Custom Thread Groups
  - 3 Basic Graphs
  - Throughput Sharing Timer
  - Dummy Sampler
  
You can refer some plugins at Google in this [link](https://jmeter-plugins.org/)
To install plugins
  - Copy them to JMETER_HOME/lib/ext
  - Use JMeter Plugins Manager

# Configuring a Test Plan
// Todo

# Collecting and Analyzing Test Results
// Todo
