# Data Flow Plan

To track the devices connected to the network should use a mix of the ARP table of the server and a database of MAC addresses to map within the network.

## Device Database Structure

```
[
  {
    "name": "Nathan",
    "addresses": [""]
  }
]
```

## How to search for the device

1. Run ARP request - parse into application
2. Search through table to find address which match
3. Compare with last seen IP find difference and update
4. Ping the device 1-3 times to check if it is online
5. Update active list of people who are here.
