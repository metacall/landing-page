# Getting Started

In this section, you will be introduced to how you can get started with your first contribution at MetaCall. As you have been already introduced to MetaCall Core, we will check out the steps for you to install the MetaCall Core on your local machine and write your first Polyglot example.

## Installation

MetaCall is a cross-platform library. It can be installed via Docker, Guix package manager or a pre-compiled tarball. As of now, we will install it via `curl` using a Shell script, which happens to be the easiest way of installation. Open your Terminal and enter the following command:

```bash
curl -sL https://raw.githubusercontent.com/metacall/install/master/install.sh | sh
```

This command will install the MetaCall CLI and now you can use the `metacall` command to kick-start the Command Line Interface. You can also build MetaCall Core, manually if in case you are using a Windows or OSX Operating System. Open your terminal and enter the following commands:

```bash
git clone --recursive https://github.com/metacall/core.git
mkdir core/build && cd core/build
cmake ..
cmake --build . --target install
```

People who are in favor of containerization, MetaCall also offers Docker Images for setup and debugging. Have a look [here](./docs.md#_71-docker-support) to get started with the same.

## Try the examples

MetaCall hosts multiple community examples. These examples serve as a great starting point for developers and users alike, who would like to see the power of MetaCall. You can run the examples on your local machine, once you have installed MetaCall successfully. Some of our past community examples are:

- [Polyglot News Article Scrapper](https://github.com/metacall/ml-news-article-scraper-example)
- [Polyglot URL Shortener](https://github.com/metacall/url-shortener-example)
- [Polyglot Currency Converter](https://github.com/metacall/currency-convert-example)
- [Polyglot Scrapper with proxy server](https://github.com/metacall/beautifulsoup-express-example)
- [PDF Generator with MetaCall](https://github.com/metacall/pdf-generator-email-sender-landing-page-example)
- [Using Telethon with NodeJS](https://github.com/metacall/telethon-nodejs-example)

All of the above examples host an appreciable `README` file documenting what the example does and how it can be launched on your local machine. Do remember that we host many other examples as well. Please check out the organization to find more examples that demonstrate the capabilities of MetaCall as a library to embed different languages.

## Make an example

Once you have played with the CLI enough and have run some examples, it is time for you to get started with building your example. With the fair understanding captured from the past examples, you can put your skills to the test by building a community example. Anything qualifies to be a community example as long as can demonstrate the following with your example:

- **Polyglot Development**: Your example shows how easy it is to combine various languages. If you are using Language X, it should be easy to combine the same with Language Y and Language Z further. X, Y and Z should be the supported languages for MetaCall Core.

- **Easy to get started with**: With Community examples, we wish to have an understanding that the developers and users find it easy to use the core and understand the features. Your example should be demonstrative of that. It can be a simple script launched through a simple driver code, that can truly demonstrate the capabilities of polyglot development.

- **Isolated Deployment**: Examples developed through MetaCall Core can be deployed via the MetaCall FaaS in form of modules. You can use deployment options on FaaS to further amplify your examples and truly demonstrate the scalability and functionality of FaaS.

Once you are done with your example, you can write a blog on how you created this example to further amplify what you created. You can also post it over the community channels to signify your recent progress. We would love to pull your code on the MetaCall organization, thus signifying your first contribution to MetaCall Open Source.
