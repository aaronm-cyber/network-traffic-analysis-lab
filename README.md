# Network Traffic Analysis Lab

## Overview
This project documents an investigation of a simulated network connectivity issue using tcpdump in an Ubuntu virtual machine. The goal was to examine packet traffic, identify successful and failed communications, and recommend troubleshooting steps.

## Lab Environment
- Ubuntu Linux 24.04 LTS
- Oracle VirtualBox
- tcpdump
- AI generated packet capture (`case_02_capture.pcap`)

  ## Scenario
  A workstation experiences failures accessing certain network resources while other network activity continues to function. The objective was to identify what the packet evidence reveals about the failure.

  ## Investigation
  The capture was analyzed using:
  ```bash
  tcpdump -r /home/aaron/case_02_capture.pcap
  ```
The analysis included identifying hosts, interpreting DNS queries, recognizing TCP three way handshakes, examining HTTP responses, and interpreting ICMP messages.

## Key Findings
- The workstation (`10.10.20.15`) demonstrated basic network connectivity.
- DNS server `10.10.23.53` successfully resolved `example.com` and `status.example.net`.
- DNS queries for `portal.internal` and `updates.internal` received ICMP UDP port 53 unreachable errors.
- The evidence indicated DNS related communication failures, but does not establish their underlying cause.

## Recommended Troubleshooting
  1. Check the DNS service for consistent operation
  2. Review DNS server logs around the time of the failed requests.
  3. Examine firewall rules affecting UDP port 53.
  4. Collect additional packet evidence and repeat the affected queries.
 
  ## Skills Practiced
     - Linux command line and tcpdump
     - DNS and TCP/IP traffice interpretation
     - ICMP and HTTP analysis
     - Network troubleshooting
     - Evidence based documentation
    
  ## Lesson
  This project strengthened my ability to follow network communications, distinguish successful traffic from errors, and document findings without assuming an unconfirmed root cause.

  ## Evidence

  ### tcpdump Packet Analysis
  ![tcpdump Packet Analysis]

  ### Full Lab Report
  [View Full Network Traffic Analysis Report (PDF)]
  
  ## Lab Transparency
  This project was conducted in a simulated lab environment using an AI generated packet capture for educational purposes.
