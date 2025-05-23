# Parallel SSH (PSSH)

PSSH (Parallel SSH) is a tool set for executing commands in parallel on multiple remote hosts. It provides parallel versions of OpenSSH and related tools, including pssh, pscp, prsync, pnuke, and pslurp.

## Features

- Parallel execution of SSH commands
- Parallel file transfers
- Support password authentication and key authentication
- Support custom timeout and parallelism
- Support output redirection
- Support color output

## System requirements

- Python 3.6 or higher
- OpenSSH client

## Install

```bash
# Install from source
python3 setup.py install
```

## How to use

### 1.Common options

- `-h, --hosts`: Specify a host list file
- `-H, --host`: Specify a single host
- `-l, --user`: Specify a username
- `-p, --par`: Set parallelism
- `-t, --timeout`: Set timeout in seconds
- `-o, --outdir`: Specify a standard output directory
- `-e, --errdir`: Specify a standard error output directory
- `-A, --askpass`: Enable password authentication
- `-i, --inline`: Display each server's output inline
- `-P, --print`: Print output in real time

### 2. Environment variables

- `PSSH_USER`: default username
- `PSSH_PAR`: default parallelism
- `PSSH_OUTDIR`: default output directory
- `PSSH_ERRDIR`: default error output directory
- `PSSH_TIMEOUT`: default timeout
- `PSSH_VERBOSE`: enable verbose output
- `PSSH_ASKPASS`: enable password authentication

## Precautions

1. Ensure that the target host is accessible via SSH
2. It is recommended to use SSH key authentication to improve security
3. Set the parallelism appropriately to avoid excessive load on the target host
4. Use the timeout option to avoid long-term command suspension

## license

BSD License 