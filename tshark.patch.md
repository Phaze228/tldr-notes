
- Output as JSON to find fields for -Y

`tshark -r {{file.pcap}} -T json`

`tshark -r {{file.pcap}} -T {{fields}} -e {{tcp}}  -Y '{{frame.len > 70}}'`
