docker-pull
===========

**docker-pull** adds statistics about known vulnerabilities on pulled image to
the `docker pull` command.

Statistics are fetched from [VulnerableContainers.org][1], a [research work by
RJGamblin][2].

![docker-pull](screenshot.png)

## How to Install

**Note:** This is an experimental tool. Use it at your own risk!

You may need to change the `DOCKER_BIN` variable in the `docker-pull` script to
reflect the location of the `docker` binary in your system (`$ which docker`)

1. Clone the repo (e.g. `/opt`)
   ```
   $ cd /opt; git clone https://github.com/PauloASilva/docker-pull
   ```
2. Create a symbolic link to
   ```
   cd /usr/local/bin; sudo ln -s /opt/docker-pull/docker-pull docker
   ```

### Dependencies

`docker-pull` requires the following tools to be installed: `tput`, `wget`,
`jq`, `sort`, `uniq` and `sed`.

## License

Copyright (c) 2019

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

[1]: https://vulnerablecontainers.org/
[2]: https://www.kennasecurity.com/one-fifth-of-the-most-used-docker-containers-have-at-least-one-critical-vulnerability
