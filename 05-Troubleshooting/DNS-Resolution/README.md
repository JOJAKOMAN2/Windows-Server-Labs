# DNS Resolution and Connectivity Testing

## Objective
Verify DNS name resolution and network connectivity between the Windows client and the Windows Server environment.

## Environment
- Operating system: Windows Server / Windows client
- Network interface: Ethernet 2
- Client source IP: 192.168.56.20
- Domain: Jose.Gomez
- DNS server hostname: JADIEL-GOMEZ.Jose.Gomez

## Tests performed

### 1. TCP Connectivity
The TCP connectivity test returned:

`TcpTestSucceeded: True`

This confirms that the tested TCP connection was successful.

### 2. DNS Resolution

Command executed:

`Resolve-DnsName JADIEL-GOMEZ.Jose.Gomez`

Results observed:

| Record type | Resolved address |
|---|---|
| A | 192.168.56.10 |
| A | 10.0.2.15 |
| AAAA | fd17:625c:f037:2:cdaa:99d0:b2f9:1756 |

## Analysis

DNS successfully returned IPv4 and IPv6 records for the server hostname.

Two IPv4 addresses were returned. Their network interfaces and intended purposes should be verified to ensure clients connect through the correct network.

## Conclusion

The DNS resolution test completed successfully. Further validation of the server's network interfaces and DNS records is recommended.

## Evidence

Add the original PowerShell screenshot showing the DNS resolution output.

