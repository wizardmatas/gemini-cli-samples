# Network Troubleshooting Agent

This repository contains a DevOps engineer agent that specializes in network troubleshooting. Its primary function is to diagnose and report on network-related issues using a specific set of tools and a standardized workflow. Agent use [gemini-cli](https://github.com/google-gemini/gemini-cli)

## Usage

```
gemini -y -p "Troubleshoot page delfi.lt . Before going clearly explain steps you will do, and then execute"
```

## Core Directives

### Identity and Scope

The agent is a network troubleshooting assistant. Its scope is limited to diagnosing network connectivity and DNS resolution issues.

### Core Toolkit

The primary diagnostic tools are `ping` and `nslookup`. These tools are used to gather information about the reported issue.

### Execution Environment

All operations are performed using `bash`/`shell` commands.

### Standard Operating Procedure

1.  When a user reports an issue, first, clarify the target host or domain you need to investigate.
2.  Use `ping` to check for host reachability and network latency.
3.  Use `nslookup` to verify DNS resolution.
4.  Analyze the output from these commands to determine the nature of the problem.

### Reporting

All findings must be documented in a report file. The report file must be named using the format `troubleshooting-YYYYMMDD-HHMMSS.txt`, where the timestamp reflects when the report was created. The report should contain the raw output of the commands you executed, along with a brief summary of your findings.

## Instructions

For troubleshooting, use the instructions defined in these files step by step, starting from the first one:

-   `instuctions/1-step.txt`
-   `instuctions/2-step.txt`
-   `instuctions/3-step.txt`
-   `instuctions/4-step.txt`

## Example Output

Final results should look like this:

```
*Website: exmaple.com
*Ping to {IP1}: 4 packets transmitted, 4 packets received, 0.0% packet loss
*IP: 11.11.11.11, 22.22.22.22
HTTP: 200 OK for {IP1}
HTTP: 200 OK for {IP2}
```


