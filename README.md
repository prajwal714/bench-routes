你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# Bench-routes

[![Build Status](https://travis-ci.com/zairza-cetb/bench-routes.svg?branch=master)](https://travis-ci.com/zairza-cetb/bench-routes)
[![Go Report Card](https://goreportcard.com/badge/github.com/zairza-cetb/bench-routes)](https://goreportcard.com/report/github.com/zairza-cetb/bench-routes)
[![Gitter](https://img.shields.io/badge/join%20discussions%20on%20gitter-%23benchroutes-green/)](https://gitter.im/bench-routes/community#)

Bench-routes is a highly scalable network benchmarking, routes performance and monitoring tool, that monitors in regular intervals the state
of the server, running as a daemon process. For more information, read the [docs](https://docs.google.com/document/d/1jGfc2eXvToRL9anzosTLQ4zJ7fdFxMGfaiDv2BYHEvw/edit?usp=sharing)

### Read the complete idea and approach [here](https://github.com/zairza-cetb/bench-routes/blob/master/approach.md).

Monitoring has been tough and with the increase in the routes used in any sophisticated project, the performance and metrics of an application are seriously affected.
With an increase in server computational models, the probability of a complete request-response cycle without any throws is nowhere close to 1. 

The primary goals of the project are:

```
1. Benchmark route
  (a) Load-handling of application on the individual route.
  (b) Test various possibilities of data in params (Permutate params), like sending an empty param
      to see how the server response behaves.
2. Analyse network performance of the hosted application irrespectively of containerization
  (a) Network ping
  (b) Jitter analysis
  (c) Packet loss
3. Log error handling capability of the application
4. Maintain a check on server-route output and alert on changes above the threshold
5. Graphical view using ElectronJS
```

For installation instructions, please head-over to [INSTALL.md](https://github.com/zairza-cetb/bench-routes/blob/master/INSTALL.md).

## Making Commits in bench-routes
Bench Routes uses DCO(Developer Certificate Origin) to certify that the contributor wrote the particular code or otherwise have the right to submit the code they are contributing to the project.For complete details on DCO  <a href="https://probot.github.io/apps/dco/" target="_blank">Click Here</a>.

Follow the below `commit` syntax to certify the code and pass the DCO test.
```
git commit -s -m <commit-message>
```

## Use of MakeFile in bench-routes
We use `make` for building and executing the program.

Follow the commands to make the development process easier:

1. Updating the dependencies: `make update`
2. Executing the application (assuming all dependencies are installed): `make run`
2. Building the application for the current OS: `make build`
3. Testing Golang code: `make test`
4. Complete testing include building for all OSs out there: `make test_complete`
5. Cleaning up the residual files: `make clean`
6. *(optional)* Check linting (assuming [golangci-lint](https://github.com/golangci/golangci-lint#install) is installed): `make lint`

## Postman Usage
1. Download [Postman](https://www.postman.com/downloads/) and Install it.
2. Create a new collection.

### To Check Service State
1. Add request
2. Select method **GET**
3. Copy and Enter below request url  
`http://localhost:9090/service-state` 
4. Send the request to url.
5. This API returns the state of the services (active or passive) in real-time.

### To Get Routes Summary
1. Add request
2. Select method **GET**
3. Copy and Enter below request url  
`http://localhost:9090/routes-summary` 
4. Send the request to url.
5. This API returns the list of all URLs/Routes that are being monitored for testing using the application.

For more information, regarding usage in different languages. Visit [Bench-Routes](https://documenter.getpostman.com/view/6521254/SzRuWqq9?version=latest).
