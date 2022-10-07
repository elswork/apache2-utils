# Apache2-utils

A [Docker](http://docker.com) file to build [apache2-utils](https://github.com/wg/apache2-utils) a set of utility programs for web servers.

> Be aware! You should read carefully the usage documentation of every tool!

Provides some add-on programs useful for any web server. These include:

 - ab (Apache benchmark tool)
 - fcgistarter (Start a FastCGI program)
 - logresolve (Resolve IP addresses to hostnames in logfiles)
 - htpasswd (Manipulate basic authentication files)
 - htdigest (Manipulate digest authentication files)
 - htdbm (Manipulate basic authentication files in DBM format, using APR)
 - htcacheclean (Clean up the disk cache)
 - rotatelogs (Periodically stop writing to a logfile and open a new one)
 - split-logfile (Split a single log including multiple vhosts)
 - checkgid (Checks whether the caller can setgid to the specified group)
 - check_forensic (Extract mod_log_forensic output from Apache log files)
 - httxt2dbm (Generate dbm files for use with RewriteMap)

## Details

| Website | GitHub | Docker Hub |
| --- | --- | --- |
| [Deft.Work my personal blog](https://deft.work) | [apache2-utils](https://github.com/elswork/apache2-utils) | [apache2-utils](https://hub.docker.com/r/elswork/apache2-utils) |

| Docker Pulls | Docker Stars | Size | Sponsors |
| --- | --- | --- | --- |
| [![Docker pulls](https://img.shields.io/docker/pulls/elswork/apache2-utils.svg)](https://hub.docker.com/r/elswork/apache2-utils "apache2-utils on Docker Hub") | [![Docker stars](https://img.shields.io/docker/stars/elswork/apache2-utils.svg)](https://hub.docker.com/r/elswork/apache2-utils "apache2-utils on Docker Hub") | [![Docker Image size](https://img.shields.io/docker/image-size/elswork/apache2-utils)](https://hub.docker.com/r/elswork/apache2-utils "apache2-utils on Docker Hub") | [![GitHub Sponsors](https://img.shields.io/github/sponsors/elswork)](https://github.com/sponsors/elswork "Sponsor me!") |

## Build Instructions
Build for amd64, armv7l or arm64 architecture (thanks to its [Multi-Arch](https://blog.docker.com/2017/11/multi-arch-all-the-things/) base image)

```bash
docker build -t elswork/apache2-utils .
```

## Usage Example

### AB Benchmark

```bash
docker run --rm elswork/apache2-utils \
ab https://www.theworldsworstwebsiteever.com/
```
or
```bash
make bench SITE=https://www.theworldsworstwebsiteever.com/
```

**OPTIONALLY** you can use these parameters before site URL:
    -c, --connections: total number of HTTP connections to keep open with
                       each thread handling N = connections/threads

    -d, --duration:    duration of the test, e.g. 2s, 2m, 2h

    -t, --threads:     total number of threads to use

    -s, --script:      LuaJIT script, see SCRIPTING

    -H, --header:      HTTP header to add to request, e.g. "User-Agent: apache2-utils"

        --latency:     print detailed latency statistics

        --timeout:     record a timeout if a response is not received within
                       this amount of time.


**[Sponsor me!](https://github.com/sponsors/elswork) Together we will be unstoppable.**

Other ways to fund me:

[![GitHub Sponsors](https://img.shields.io/github/sponsors/elswork)](https://github.com/sponsors/elswork) [![Donate PayPal](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/donate/?business=LFKA5YRJAFYR6&no_recurring=0&item_name=Open+Source+Donation&currency_code=EUR)