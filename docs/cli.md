# MetaCall Command Line Interface

This repository provides a Docker fallback option for architectures and operative systems that are still not supported by [metacall/distributable](https://github.com/metacall/distributable) for installing a portable CLI by means of Docker.

## Install

For installing we need to pull the image.

```sh
docker pull metacall/cli
```

Then set up the `metacall` command as an alias. This snippet of code must be pasted in your `.bashrc` or `.zshrc`:

```sh
alias metacall='function mc() { docker run --rm --network host -e "LOADER_SCRIPT_PATH=/metacall/source" -w /metacall/source -v `pwd`:/metacall/source -it metacall/cli $@; }; mc'
```

## Build

In case of you want to build it yourself. The `sed` is used to remove unused layer from the Dockerfile. The build is done disabling the cache of the CLI download layer so it always will download the latest version of the CLI.

```sh
sed 's/FROM metacall/#FROM metacall/' Dockerfile > Dockerfile.build
docker build --build-arg DISABLE_CACHE=`date +%s` -t metacall/cli -f Dockerfile.build .
```

## Using a Different Version

In case of you want to patch the CLI version with a new one, a simple way of doing it is to download the tarball you want to patch from here (https://github.com/metacall/distributable/releases). Then untar it into `/` with **root permissions**, give user permissions and mount that into the volume when running the CLI:

```sh
tar -xvf metacall-tarball-linux-amd64.tar.gz -C /
chown -R your_user:your_user /gnu
alias metacall='function mc() { docker run --rm --network host -e "LOADER_SCRIPT_PATH=/metacall/source" -w /metacall/source -v `pwd`:/metacall/source -v /gnu:/gnu -it metacall/cli $@; }; mc'
```

## Troubleshooting

- The CLI does not found the packages I have recently installed with `metacall pip3 install -r requirements.txt`:
  ```sh
  alias metacall='function mc() { docker run --rm --network host -e "LOADER_SCRIPT_PATH=/metacall/source" -w /metacall/source -v `pwd`:/metacall/source --entrypoint sh -it metacall/cli; }; mc'
  ```
  Modify the entry point to get a bash so the data can be shared between commands.
