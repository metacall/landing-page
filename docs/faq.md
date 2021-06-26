# FAQ

**MetaCall Frequently Asked Questions.**

Last update: April 6, 2019

<!-- TOC -->

- [FAQ](#faq)
  - [Section A: General](#section-a-general)
    - [What is MetaCall?](#what-is-metacall)
    - [What is MetaCall used for?](#what-is-metacall-used-for)
    - [Does Function Mesh application architecture pattern benefit from MetaCall technology?](#does-function-mesh-application-architecture-pattern-benefit-from-metacall-technology)
    - [There is any technology similar to MetaCall Function Mesh?](#there-is-any-technology-similar-to-metacall-function-mesh)
    - [Is MetaCall a Polyglot?](#is-metacall-a-polyglot)
    - [Who is the target audience for MetaCall?](#who-is-the-target-audience-for-metacall)
    - [Which applications / workloads have the potential to benefit the most from MetaCall?](#which-applications--workloads-have-the-potential-to-benefit-the-most-from-metacall)
    - [Can MetaCall be used for SOA / Legacy / Monolithic / Micro-services architecture-based applications? Or is it suited for only some of these application architectures?](#can-metacall-be-used-for-soa--legacy--monolithic--micro-services-architecture-based-applications-or-is-it-suited-for-only-some-of-these-application-architectures)
  - [Is MetaCall meant for private function calls or also for public APIs?](#is-metacall-meant-for-private-function-calls-or-also-for-public-apis)
    - [Is there any benchmark data to show how MetaCall compares with alternative technologies?](#is-there-any-benchmark-data-to-show-how-metacall-compares-with-alternative-technologies)
      - [MetaCall vs HTTP Servers Benchmark](#metacall-vs-http-servers-benchmark)
      - [MetaCall FFI vs Runtime Call Benchmark](#metacall-ffi-vs-runtime-call-benchmark)
    - [What are some of the benefits associated with adopting MetaCall?](#what-are-some-of-the-benefits-associated-with-adopting-metacall)
    - [Are there any challenges associated with MetaCall adoption?](#are-there-any-challenges-associated-with-metacall-adoption)
    - [How is MetaCall implemented? What is its high-level architecture?](#how-is-metacall-implemented-what-is-its-high-level-architecture)
    - [What is MetaCallâ€™s scaling model?](#what-is-metacalls-scaling-model)
    - [Is MetaCall cross-platform?](#is-metacall-cross-platform)
    - [What are some of the MetaCall use cases and examples?](#what-are-some-of-the-metacall-use-cases-and-examples)
    - [List some of the benefits of MetaCall.](#list-some-of-the-benefits-of-metacall)
    - [How does MetaCall benefit Legacy code migration or evolution?](#how-does-metacall-benefit-legacy-code-migration-or-evolution)
    - [How does MetaCall help in progressive migration instead of refactoring and rebuilding legacy solutions?](#how-does-metacall-help-in-progressive-migration-instead-of-refactoring-and-rebuilding-legacy-solutions)
    - [How is MetaCall different in terms of number of functions that can be invoked or called per file?](#how-is-metacall-different-in-terms-of-number-of-functions-that-can-be-invoked-or-called-per-file)
    - [How does MetaCall offer the benefit of being a common solution for gateway, SQS?](#how-does-metacall-offer-the-benefit-of-being-a-common-solution-for-gateway-sqs)
    - [Are there any disadvantages of using MetaCall?](#are-there-any-disadvantages-of-using-metacall)
    - [How does MetaCall benefit developer productivity?](#how-does-metacall-benefit-developer-productivity)
    - [Who deploys MetaCall and scales it at runtime?](#who-deploys-metacall-and-scales-it-at-runtime)
    - [Is MetaCall pluggable and supports different protocols?](#is-metacall-pluggable-and-supports-different-protocols)
    - [What kind of FaaS does MetaCall support?](#what-kind-of-faas-does-metacall-support)
    - [Are there any specific industries or applications that can benefit from MetaCall based application designs?](#are-there-any-specific-industries-or-applications-that-can-benefit-from-metacall-based-application-designs)
    - [How does MetaCall model impact contemporary application design and architecture?](#how-does-metacall-model-impact-contemporary-application-design-and-architecture)
  - [Section B: MetaCall vs. alternative solutions](#section-b-metacall-vs-alternative-solutions)
    - [How is MetaCall different from REST and RPC?](#how-is-metacall-different-from-rest-and-rpc)
    - [What are the key MetaCall differentiations factors from say **OpenFaaS**, **Zeit**, **Kubeless**, other competing technologies?](#what-are-the-key-metacall-differentiations-factors-from-say-openfaas-zeit-kubeless-other-competing-technologies)
    - [What is the difference between MetaCall and AWS Lambda?](#what-is-the-difference-between-metacall-and-aws-lambda)
    - [Is MetaCall similar to AWS Lambda, Microsoft Azure Functions and Twilio?](#is-metacall-similar-to-aws-lambda-microsoft-azure-functions-and-twilio)
    - [How does MetaCall provide value add that is beyond what other similar services such as AWS Lambda offer?](#how-does-metacall-provide-value-add-that-is-beyond-what-other-similar-services-such-as-aws-lambda-offer)
    - [How does MetaCall simplify the complex and time-consuming application restructuring required for serverless architectures based on AWS Lambda, Microsoft Azure Functions or Google Functions?](#how-does-metacall-simplify-the-complex-and-time-consuming-application-restructuring-required-for-serverless-architectures-based-on-aws-lambda-microsoft-azure-functions-or-google-functions)

<!-- /TOC -->

---

## Section A: General

### What is MetaCall?

MetaCall helps you build serverless applications using a more fine-grained, scalable and NoOps oriented FunctionMesh instead of ServiceMesh and DevOps approach. MetaCall automagically converts your code into a **[Function Mesh](https://medium.com/@metacall/function-mesh-architecture-c0304ba4bad0)** and auto-scales individual hot parts or functions of your app.

MetaCall not only helps to simplify application development but also speeds up time to market. Developers can focus purely on code and business logic instead of expending expensive development cycles on DevOps.

### What is MetaCall used for?

- The purpose of MetaCall is to integrate local development with function-mesh transparently.

- MetaCall enables a new, smarter and productive way to develop distributed systems. It is a library that allows you to execute code across boundaries â€“ be it language, process, pod, container, node or server boundaries. Your code could be in language X and it can invoke functions implemented in languages X, Y, and Z where X, Y, Z are the set of supported languages in MetaCall core.

- CRUD via HTTP in REST APIs is a form of RPC with limited functions. MetaCall extends the abstraction to any function that can be called remotely and not just limited to semantics of CRUD. (Note REST, i.e., CRUD over HTTP is sort of a degenerate form of RPC). Over and above these functions could be implemented in a different programming language and running on a different pod / container / server / node distributed geographically.

### Does Function Mesh application architecture pattern benefit from MetaCall technology?

Function Mesh is a new transparent way to inter-connect serverless functions. Function Mesh enables building of complex distributed systems while efficiently scaling only the hot functional parts of the system. MetaCall is an enabling technology that helps to build the function gateway of sorts, under the covers. The only thing developers need to care about is writing a small configuration file indicating what code they want to publish and the function gateway will be automatically created by MetaCall. Scaling up and down of MetaCall instances happens in an automatic manner governed by certain configurable limits such as \$\$ spent for resources, response time or latencies.

Function Mesh introduces a new way of development. It is possible to develop a complete monolith service and this will be scaled depending on the hot parts of the application. The Function Mesh will grow and subdivide parts of the monolith if needed or shrink when the workload is lower. At the same time it is non-intrusive. This means you can code normal applications without needing a new complete framework or architecting the code or infrastructure. At the same time, that code can be tested and debugged locally without needing clusters like Kubernetes or complex environments with many layers of abstraction. The developer can use existing common tools, debuggers and test runners. You can build a complete distributed system in a single project without worrying about the infrastructure.

### There is any technology similar to MetaCall Function Mesh?

Nowadays it is possible to implement Service Mesh in your architecture. Service Mesh is a practical way to interconnect services in your architecture. You can use tools like [Istio](https://istio.io/) (Service Mesh) and [OpenFaaS](https://www.openfaas.com/) (FaaS) on top of [Kubernetes](https://kubernetes.io/) (Orchestrator) to build your architecture. Other alternatives are appearing, like [OpenFaaS Flow](https://github.com/s8sg/faas-flow) to interconnect functions.

This solutions have drawbacks. Kubernetes itself is a really complex tool that has a difficult learning curve, and OpenFaaS and Istio introduce even more complexity and knowledge. The resulting architecture can be powerful, but really difficult to build. Apart from this, testing the system must be done in the cloud, or in a powerful local machine, to handle the whole cluster and the consumption of all this systems. In addition, Service Mesh has the drawback that it injects a proxy for each pod or service instance, duplicating the size of the processes the cluster must handle and adding an intermediate layer between the functions.

The idea MetaCall Function Mesh is to unify the development. MetaCall allows a non-intrusive way to develop this architecture, without handling all cluster and complex tools by yourself (no more yaml abuse). In addition, in the Function Mesh each function is a load balancer and proxy at the same time. It takes advantage of concurrency and it also can be scaled horizontally, creating a uniform matrix of functions interconnected. Three levels of scalability that can drastically reduce costs, improve performance, and simplify the life of the developer.

### Is MetaCall a Polyglot?

**[MetaCall Core](https://github.com/metacall/core)** can be seen as a Polyglot. A multi-language interpreter that can execute different programming languages at the same time. But MetaCall itself is not a MetaVirtualMachine, in fact it only provides foreign function interface calls between programming languages. It can help integrate functionality across application components written in different languages. We are using it to build our core for the FaaS. By this way we achieve an high performance of the execution of the calls.

For a complete list of supported languages, refer to **[MetaCall Language Support - Backend](https://github.com/metacall/core#2-language-support-backends)**.

For testing performance of MetaCall calls, refer to **[MetaCall Benchmarks](https://github.com/metacall/core/tree/develop/source/benchmarks)**.

### Who is the target audience for MetaCall?

**Target Audience**: Developers, Solution Architects.

**Key Use case**:

MetaCall is useful for enterprises that need to migrate legacy or traditional non-micro-services architecture based distributed application solutions (monolithic, SoA) without refactoring the entire code base. It is also very useful for developerâ€™s productivity and eliminates the need to setup complex K8s cluster for testing code in production.

MetaCall enables developers to test the code in local just as it would run in production â€“ saves time and resources and brings solutions to market faster.

### Which applications / workloads have the potential to benefit the most from MetaCall?

| Application Type                                                                                                                               | Benefits with MetaCall | Comments                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------: | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Application with persistent or long-lived interactions and inter-service connections for performing tasks that can scale up or down quickly    |          Yes           | `Need confirmation from V`                                                                                                                                |
| Applications with short term intermittent communication across components or micro-services where these interactions can scale up or down fast |          Yes           | `Need confirmation from V`                                                                                                                                |
| Applications that are not front-end facing but in deeper end of the stack and deal with caches, databases and intermediary services            |          Yes           | `Need confirmation from V`                                                                                                                                |
| Applications with bi-directional data flow                                                                                                     |           ?            |                                                                                                                                                           |
| CPU-centric applications                                                                                                                       |           ?            |                                                                                                                                                           |
| I/O intensive applications                                                                                                                     |           ?            |                                                                                                                                                           |
| Message Broker based big data applications? (ETL, Hadoop, Spark, Flink â€“ data warehousing apps)                                              |           ?            |                                                                                                                                                           |
| Real time messaging application for Big Data Analytics                                                                                         |           ?            | _Need confirmation from V_ **[Reference: Real time messaging for analytics](https://medium.com/@natemurthy/rest-rpc-and-brokered-messaging-b775aeb0db3)** |

---

### Can MetaCall be used for SOA / Legacy / Monolithic / Micro-services architecture-based applications? Or is it suited for only some of these application architectures?

MetaCall can be used for either of the above. It is not limited to an application architecture type.

## Is MetaCall meant for private function calls or also for public APIs?

Yes, you can secure your APIs with MetaCall or maintain them public from the Dashboard.

### Is there any benchmark data to show how MetaCall compares with alternative technologies?

Here is some of the available benchmark data for MetaCall (Beta). More benchmarking tests are underway and will be updated shortly.

#### MetaCall vs HTTP Servers Benchmark

**Benchmark Description:**

Simple function that merges two strings using the following technologies:

1. Flask (Python HTTP server)
2. Express (Node.js HTTP server)
3. MetaCall with Python
4. MetaCall with Node.js
5. NginX (no back-end at all)

**Specs:**

- [Intel Xeon processor with 10 cores and 20 threads, 13.75M cache, 3.3GHz processor, 32GB RAM â€“ server](https://ark.intel.com/content/www/us/en/ark/products/125042/intel-xeon-w-2155-processor-13-75m-cache-3-30-ghz.html).
- [QEMU Virtual Machine](https://www.qemu.org/) with 10 threads assigned and 16GB RAM with Debian Stretch as guest OS.
- [wrk2](https://github.com/giltene/wrk2) as benchmarking tool.

**Results:**

|      Software      | Requests/sec | Transfer/sec |    Errors     |
| :----------------: | :----------: | :----------: | :-----------: |
|       Flask        |    614.82    |   100.87KB   | 1715 Timeouts |
|      Express       |   6433.61    |    1.39MB    | 652 Timeouts  |
| MetaCall (Python)  |   11620.65   |    1.80MB    |     None      |
| MetaCall (Node.js) |   8190.71    |    1.27MB    |     None      |
|       NginX        |   14224.61   |    2.48MB    |     None      |

**Conclusions:**

- MetaCall with Node.js is 1.3-1.4X faster than Express (Node.js HTTP server).
- MetaCall with Python is 17X to 30X faster than Flask (Python HTTP server).
- MetaCall with Python is 2X faster than MetaCall with Node.js. Typically, Express is much faster than Flask because it is I/O focused, but using MetaCall Python code outperforms Node.js.
- MetaCall has no errors in comparison to Flask or Express.

#### MetaCall FFI vs Runtime Call Benchmark

**Benchmark Description:**

Comparison of a Python C API call (hard-coded) versus a MetaCall call (ffi). No connection used, this is focused to see what is the overhead of MetaCall when executing calls between run-times. No optimization was used when compiling MetaCall (debug mode and all call optimizations disabled). One million calls was tried with two long integers for each call as an argument, and another long integer as a return value. The test has been done using only one thread, although the VM has more than one assigned to it.

**Specs:**

- Intel Core i5-4210M CPU @ 2.60GHz, 8GB RAM â€“ laptop.
- VirtualBox Virtual Machine with 2 threads and 3GB of RAM with Debian Stretch as guest OS.
- Google Test and Google Bench as benchmark software.

**Source:**

- [MetaCall Core Benchmarks](https://github.com/metacall/core/tree/develop/source/benchmarks).

**Results:**

|                Software                 |  Time  |  Bandwidth  |    Calls/sec     |
| :-------------------------------------: | :----: | :---------: | :--------------: |
|              Python C API               | 544 ms | 42.0545MB/s | 1.75227M items/s |
| MetaCall Python Variadic Arguments Call | 988 ms | 23.1689MB/s | 988.54k items/s  |
|  MetaCall Python Array Arguments Call   | 903 ms | 25.353MB/s  | 1081.73k items/s |

**Conclusions:**

- Python C API performs 1.7M calls per second versus 1.081M of MetaCall (Array Arguments Call).
- There is still room for improvement and optimization with MetaCall, at least 1.5X times the current performance.
- Although MetaCall FFI is slower than hard-coded Python C API calls it stills does 1M calls per core per second. This means that if we put it on a FaaS or HTTP server, the bottleneck will be 1M calls per thread per second, which is far away from NginX performance in terms of requests per second.

### What are some of the benefits associated with adopting MetaCall?

Following is a placeholder answer, we need to refine it as per V's inputs.

- MetaCall eases the DevOps and deployment issues associated with applications built using Micro-services architecture and deployed using containers, orchestrated via K8s. It allows testing of same code in local environment. The same code runs in distributed environment.
- MetaCall helps enterprises simplify and evolve DevOps into NoOps with the simplicity of deployment and automation.
- Polyglot Engineering â€“ Support for multiple languages â€“ Multi-lingual â€“ helps integrate various programming languages. This helps communication across application components developed in different languages.
- Helps to integrate Legacy applications in cloud and hybrid environments via phased migration instead of long tedious refactoring
- Removes dependency on third party solutions such as AWS Lambda

### Are there any challenges associated with MetaCall adoption?

- MetaCall uses QUIC (HTTP/3) technology underneath. As of **[November 2018](https://www.zdnet.com/article/http-over-quic-to-be-renamed-http3/)**, 31.2% of top 10 million websites support HTTP/2 and only 1.2% sites support QUIC. Is this going to be a limiting factor for MetaCall adoption?

### How is MetaCall implemented? What is its high-level architecture?

MetaCall implementation uses a higher-level protocol (QUIC / HTTP3) to reduce RPC overheads. It uses a high-performance multi-core asynchronous I/O model.

### What is MetaCallâ€™s scaling model?

MetaCall has unique scaling model that is more granular and more compute resource-efficient than micro-services and REST based API interaction models. MetaCall can scale at 3 levels â€“ per process, per pod and per function-mesh. Basically, it allows you to do more work with less resources and enables finer-grained resource utilization. {Any benchmark run numbers here would be useful â€“ say with MetaCall, xyz micro-services benchmark ran 5X times faster than without MetaCall.}

### Is MetaCall cross-platform?

MetaCall is a cross platform architecture â€“ it is designed to work in multiple platforms. Current tested platforms:

| Platform |                     Version                     | Architecture |
| :------: | :---------------------------------------------: | :----------: |
| Windows  |                    7, 8, 10                     | x86, x86-64  |
|  Linux   | Debian (8, 9, 10), Ubuntu (14.04, 16.04, 18.04) |    x86-64    |
|  MacOs   |                      10.14                      |    x86-64    |

### What are some of the MetaCall use cases and examples?

**MetaCall use cases** â€“ TBD

**MetaCall examples** - see Auth Function Mesh and refer to the **[examples folder in GitHub.](https://github.com/metacall/examples)**

### List some of the benefits of MetaCall.

- Developer Productivity

  - MetaCall enables developers to test their code locally while the same code can be run across clusters at runtime.
  - It saves on test/debug resources and helps with developer productivity.
  - During development and testing, there is no dependency on launching K8s cluster, or installing Minikube or testing by using AWS/cloud resources.

- Saves time, lowers costs

  - MetaCall reduces the need of additional test resources required for cluster setup and testing
  - Helps to save cloud resource costs

- Simplifies and speeds up Legacy code and cloud technologies integration

* Instead of total refactoring to bring legacy code to cloud, MetaCall allows phasewise and staged migration of chunks of functionality to contemporary cloud application architectures models as it allows function calls across language, node and process boundaries.

### How does MetaCall benefit Legacy code migration or evolution?

To bring Legacy code to cloud, or to evolve it using newer application architecture models such as micro-services, you need a service like Lambda. Instead, you can use MetaCall and without rewriting legacy code, migrate some or all its functionality to the cloud.

### How does MetaCall help in progressive migration instead of refactoring and rebuilding legacy solutions?

Let us consider this example as shown in figures below:

|                     ![Phase Approach][phase]                     |
| :--------------------------------------------------------------: |
| _Function A calls functions B, C and D, all implemented in PHP _ |

[phase]: https://raw.githubusercontent.com/metacall/faq/master/fig/fn1.png

Lets say all functions are written in PHP, and Â´Fn AÂ´ calls Â´Fn BÂ´, Â´CÂ´ and Â´DÂ´.
Now you want to update your code with a brand new Node.js funcion Â´Fn C'Â´.
With MetaCall, you can progressively transfer your calls from Â´Fn CÂ´ to Â´Fn C'Â´ with ease, allowing you to migrate legacy code in production.
Refer to figures below that show phased migration of PHP code to Node.js:

|                  ![Phase Approach1][phase1]                   |     ![Phase Approach2][phase2]      |          ![Phase Approach3][phase3]          |
| :-----------------------------------------------------------: | :---------------------------------: | :------------------------------------------: |
| _Function C is implemented in Node.js and rest code is as is_ | _Function B is migrated to Node.js_ | _Function B, C and D are all in Node.js now_ |

[phase1]: https://raw.githubusercontent.com/metacall/faq/master/fig/fn2.png
[phase2]: https://raw.githubusercontent.com/metacall/faq/master/fig/fn3.png
[phase3]: https://raw.githubusercontent.com/metacall/faq/master/fig/fn4.png
[phase4]: https://raw.githubusercontent.com/metacall/faq/master/fig/fn5.png

Without MetaCall, you will need 6 months or so to move legacy code into new node.js or other models before you can verify and test. With metacall, you can do it in chunks â€“ it helps with phased migration.

As indicated in the figure above, with MetaCall, you donâ€™t need two teams â€“ one to maintain legacy and another to refactor the code and make it work again using newer design and application architecture models. Helps agile and reduces TTM.

### How is MetaCall different in terms of number of functions that can be invoked or called per file?

Nowadays when you do functions, you can only do one function per file. MetaCall can do N functions per file. MetaCall allowsyou to write multiple functions in the same deployment. You can keep monolithic architecture or micro-services architecture and MetaCall will slice everything. Monolith refer to pre MSA or SoA application architecture. {Need to highlight the benefit of this â€“ how does this help developer , project, business}

### How does MetaCall offer the benefit of being a common solution for gateway, SQS?

_Answer to be provided by V_

### Are there any disadvantages of using MetaCall?

Lots of upside of MetaCall â€“ downside â€“ a small amount of resource is always consumed â€“ to avoid cold starts.

### How does MetaCall benefit developer productivity?

MetaCall simplifies test and debugging which is a nightmare in distributed application development. Test in local and the same code runs exactly the same way in production â€“ across process, pod and container boundaries. During test it runs local. So no need to test in dev and again in production.

### Who deploys MetaCall and scales it at runtime?

Self â€“ automated? There is way to limit resource consumption â€“ say by \$\$\$ or number of replicas etc. How? {_Elaborate with teh help of V_}

### Is MetaCall pluggable and supports different protocols?

MetaCall implementation has two interfaces â€“ on caller side the function gateway uses simple http (for now) â€“ in future it could be pluggable so it could use GraphQL or XML or WebSockets. At the other end, for function level communication or function gateway, it uses JSON-RPC. That could be pluggable too â€“ it could use QUIC or gRPC or RabbitMQ â€“ whichever works better for the user in terms of solution performance, required communication bandwidth and latency.

### What kind of FaaS does MetaCall support?

_Answer TBD_

### Are there any specific industries or applications that can benefit from MetaCall based application designs?

MetaCall is not industry or application specific solution. It is a newer, better model for bu
ilding your Function Mesh. (More details TBD by V)

### How does MetaCall model impact contemporary application design and architecture?

Application architectures have evolved from traditional monolithic applications and SoA architectures to applications built using micro-services architecture. The next step in evolution in serverless and Functions â€“ FaaS. The granularity of application â€˜execution-unitâ€™ has become finer and finer at each step of evolution. Consequently, application complexity has exploded and begun to impact application development and distributed application architectures.

Application granularity and resultant complexity is a disadvantage to distributed application development and testing process and a big drain on compute resources. Ideally, this granularity ought to be transparent to impart its benefits seamlessly to modern applications â€“ for example â€“ efficient and optimal consumption of underlying compute and cloud resources and services. This granularity, ideally, should not reside in the hands of the developer. Instead, it should be part of the underlying infrastructure.

With MetaCall FaaS model, you can maintain your traditional monolithic applications or contemporary micro-services-based architectures, gain the benefit of FaaS granularity without having to bother about application restructuring or developmental complexity. Your legacy code and old big architectures can be migrated to serverless and FaaS models, fully distributed by functions easily with the use of MetaCall and without needing to refactor it, or spending extra resources in development, DevOps or specialized serverless developers.

## Section B: MetaCall vs. alternative solutions

### How is MetaCall different from REST and RPC?

If you look closely, REST APIs comprise of CRUD (Create, Read, Update, Delete) operations using HTTP. It is sort of RPC with limited functions the CRUD. MetaCall extends this abstraction to any function that can be called remotely and not just limited to semantics of CRUD. In other words, REST, ie, CRUD over HTTP is sort of a degenerate form of RPC. In addition, these functions could be implemented in a different programming language and may be running on a different pod or container or node or server which is distributed geographically. TBD - How MetaCall is different from RPC or is it?

## How is MetaCall same or different or better than pure REST and RPC?

- As compared to REST/HTTP method, RPC is simpler and mature, **[request response nature helps in tracing](https://medium.com/@natemurthy/rest-rpc-and-brokered-messaging-b775aeb0db3)** the calls in large scale distributed systems. Does MetaCall assist, in any way, with debugging and tracing issues in distributed solutions?
- Defining interaction with services across process and server boundaries is richer with RPC than with REST limited by CRUD semantics.
- RPC is suitable for one-one or one-many communications. Many to one such as in data streaming, fan-in and fan-out is a tricky one â€“ with MetaCall â€“ the implementation addresses this (?)
- MetaCall is better than pure RPC as it provides function gateway functionality and more scalable and higher in performance than pure RPC.

### What are the key MetaCall differentiations factors from say **[OpenFaaS](https://www.openfaas.com/)**, **[Zeit](https://zeit.co/)**, **[Kubeless](https://kubeless.io/)**, other competing technologies?

Refer to the picture below. It shows how MetaCall differs from competition:

| ![MetaCall Competition][metacall-compet] |
| :--------------------------------------: |
|        _MetaCall vs. Competition_        |

[metacall-compet]: https://raw.githubusercontent.com/metacall/faq/master/fig/metacall-compet.png

### What is the difference between MetaCall and AWS Lambda?

Unlike Lambda, MetaCall does not have cold starts. Refer to the figures below:

|       ![Lambda Model][lambda]        |
| :----------------------------------: |
| _Function scaling model with Lambda_ |

[lambda]: https://raw.githubusercontent.com/metacall/faq/master/fig/lambda.png

|      ![MetaCall Model][metacall]       |
| :------------------------------------: |
| _Function scaling model with MetaCall_ |

[metacall]: https://raw.githubusercontent.com/metacall/faq/master/fig/metacall.png

With Lambda, you can have two or more layers of LB to scale up function and obtain function mesh â€“ see figure. With MetaCall, you can have any-to-any function mesh and it is much less expensive. In MetaCall model, each function also acts as a gateway with the help of MetaCall library. This tremendously helps in scaling and everything is integrated. No third party products are required for integrating across languages, platforms and components or routing function calls.

### Is MetaCall similar to AWS Lambda, Microsoft Azure Functions and Twilio?

AWS Lambda and Microsoft Azure functions are generic serverless platforms that can be used to create FaaS solutions. Twilio is a cloud-based enterprise contact centre software platform which is specialized for communications code (SMS, Text, Voice) and allows creation of Twilio based apps for contact center, marketing and customer engagement.

MetaCall is similar to AWS Lambda and Azure functions in the sense that it also enables you to create FaaS based solutions. However, the approach is very different. Unlike AWS or Microsoft, MetaCall does not host and handle these functions via triggers. MetaCall automagically converts your code into a **[Function Mesh](https://medium.com/@metacall/function-mesh-architecture-c0304ba4bad0)** and auto-scales individual hot parts or functions of your app. Both Lambda and Azure Functions are similar in functionality as they propose to segment the application architecture in order to scale only the parts that require scaling, thus making consumption efficient with pay-per-function-use pricing model. Unlike these two, MetaCall is not cloud provider proprietary as it can work for applications that are distributed across cloud, on-premises and even hybrid applications.

### How does MetaCall provide value add that is beyond what other similar services such as AWS Lambda offer?

In this question, we will try to answer the following queries related to MetaCall versus other similar technologies:

- Applications today are comprised of various moving parts in order to have scalable, efficient systems. Does MetaCall help in any way to replace any or all of these multiple moving parts or simplify them?

- When and how does MetaCall decide to optimize certain application actions?

- How does MetaCall based application compare with an optimized application system built using various AWS functionalities including Lambda? Is it time saved to deployment? Is one better than the other in the long run? What are the features that separate MetaCall from the rest?

Since it first appeared in 2014, AWS Lambda function implementation has not changed much. Microsoft Azure and Google cloud implemented very similar functions. The main drawback of these technologies as compared to MetaCall are detailed below:

- Current Lambda implementations are handlers in the form of:

```
exports.handler = async (event) => {
    return {
        statusCode: 200,
        headers:{
            "Content-Type": "text/html"
        },
        body: "Hello",
    };
};
```

Handlers are **[different](https://softwareengineering.stackexchange.com/questions/205846/difference-between-trigger-handler-and-callback)** from events or a function (callback). This handler is similar to the ones that exist in micro-services. When you use AWS Lambda, besides handlers, you will need to use AWS API Gateway in order to provide a valid REST endpoint to the Lambda handler. This complicates the problem multi-fold. Although it offers high granularity in terms of resource consumption, it imperates the use of other AWS services to make it work. Eventually, your application or solution will have to be split into many handlers, making it harder to manage.

For example, 10 lambda functions require 10 separate deployments and 10 additional entries into the API Gateway. If you consider Database or Message Queue service implementations, then this resource and service dependency list begins to grow even further. Now imagine, if we try to inter-connect other kinds of Lambdas to build a complete application, it just gets more and more complex.

MetaCall deals with callback or a function which is very different from a handler. A function is a piece of executable code that is passed as an argument to other code, which is expected to call back (execute) the argument at some convenient time. The invocation may be immediate as in a synchronous callback, or it might happen at later time as in an asynchronous callback.

MetaCall functions look like as shown below:

```
exports.hello_world = () => {
    return "Hello";
}
```

Instead of looking like a handler, a MetaCall function looks like a normal function, that can be unit tested locally with common development tools. There is no need of extra framework or resource deployment in order to debug it or test it. Also, you can add more functions in the same file and they will be deployed separately.

If you want to call other functions, you just have to call it like a normal function:

```
import { other_function } from 'lib';

    exports.hello_world = () => {
        return other_function();
    }
```

This will build a function mesh for you. The function â€˜other_functionâ€™ may be executed on another peer, and the network resolution, scalability, and everything will be automatically taken care of by MetaCall.

Following are a list of benefits that MetaCall usage brings in to the developers and modern application development process:

1. Developers can build monolithic applications that will be fully distributed through MetaCall model.

2. MetaCall brings in an integrated API Gateway along with the functions, so there is no need for updating API Gateways for each function as in the case of AWS Lambda.

3. MetaCall allows application developers to write functions that can be tested locally, and validated globally in one shot. This is because they are normal functions and after being upload to the FaaS they will be automatically scaled. Developers do not have to first test and then verify the deployment in production.

4. With MetaCall usage, the organizationâ€™s development lifecycle can be speeded up. The developer encounters less friction when implementing the software.

5. MetaCall abstracts and hides the nuances and differences across multiple cloud vendors. With MetaCall, the developer will not be required to understand AWS or any other vendor specific implementation models because MetaCall integrates with repositories seamlessly.

6. MetaCall pricing is transparent and simpler. You will not have to deal with high segmentation and obfuscated costs. You will be able to see all telemetry and consumption of your code.

Here is how MetaCall overcomes some of the drawbacks associated with AWS Lambda:

- Metacall does not have **[typical serverless cold start](https://thenewstack.io/how-cold-starts-impact-serverless-performance/)** performance issues.

- MetaCall automatically builds all dependencies with your functions in a standard way, using existing package managers.

- MetaCall is simple to use as it integrates into normal developer code, without complex frameworks, thus reducing vendor lock-in.

- Unlike AWS Lambda or typical serverless models, MetaCall enables you to test code locally and run it, later on, in the FaaS, with equivalent distributed execution without having to test it twice â€“ once locally and then in production.

- MetaCall scales hot parts of your application depending on the workload and the function calls for each function published in the function mesh. The function mesh can be subdivided or compressed depending on the workload.

- MetaCall allows persistence though functions just by exporting common objects or arrays in the code.

In short, instead of having to use AWS API Gateway, DynamoDB, Lambda, Elastic Load Balancer, Simple Queue Service... (among others), MetaCall solves application scaling and distribution problem at the same time, without DevOps. There is no learning curve or new framework needed for MetaCall use. Local testing capability significantly improves development time and cuts down on resource usage. The function mesh model allows for a more effective way of scaling, so we can scale horizontally, vertically and in a new third dimension introduced by the code splitting.

All this is taken care of by MetaCall, with no additional cost or new knowledge required for the developer.

Besides the above, with MetaCall, there is an extra benefit: your existing code can be migrated to MetaCall easily, because as it does not need a new framework. MetaCall can consume classical functions. Migrations to MetaCall based FaaS environment can be done automatically.

### How does MetaCall simplify the complex and time-consuming application restructuring required for serverless architectures based on AWS Lambda, Microsoft Azure Functions or Google Functions?

One of core objectives of MetaCall is to simplify application migration to FaaS. Most of the problems related to ‘fitting’ an existing application into FaaS model are caused by the limitations of current FaaS designs. With the cutting-edge design of MetaCall you will be able to migrate a monolithic application into FaaS easily.
