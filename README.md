Description
DNS Lookup Tool is a powerful and flexible Python script for performing DNS queries.
It can retrieve a variety of DNS records (A, AAAA, MX, NS, TXT, etc.), supports DNS over HTTPS (DoH), and can attempt zone transfers (AXFR) if allowed.

This tool is ideal for network administrators, security testers, and anyone curious about DNS information.

Features
Query multiple DNS record types (A, AAAA, MX, NS, TXT, CNAME, SOA, PTR).

Support for custom DNS servers.

Support for DNS over HTTPS (using Cloudflare DNS).

Attempt AXFR Zone Transfers (if the DNS server allows).

Display results in a beautiful Rich-style table.

Colorful and readable terminal output.

ASCII Art banner with pyfiglet.

📦 Requirements
Before running the script, install the required Python libraries:

pip install -r requirements.txt
Or manually:

pip install dnspython requests rich colorama pyfiglet
Required Libraries:

dnspython

requests

rich

colorama

pyfiglet

How to Use
Clone the repository:

git clone https://github.com/yourusername/dns-lookup-tool.git
cd dns-lookup-tool
Install dependencies:

pip install -r requirements.txt
Run the tool:

python dns_lookup.py -d example.com
📋 Command-line Options

Option	Description	Example
-d, --domain	Domain(s) to query (can specify multiple)	-d example.com
-t, --type	DNS record type (e.g., A, AAAA, MX, TXT)	-t A
-s, --server	Custom DNS server (e.g., 8.8.8.8)	-s 8.8.8.8
--axfr	Attempt Zone Transfer (requires -s option)	--axfr
--doh	Use DNS-over-HTTPS (Cloudflare DNS)	--doh
📌 Examples
Simple Lookup:

python dns_lookup.py -d example.com
Lookup specific record type (e.g., MX):

python dns_lookup.py -d example.com -t MX
Using a custom DNS server:

python dns_lookup.py -d example.com -s 1.1.1.1
DNS over HTTPS (DoH):

python dns_lookup.py -d example.com --doh
Attempt Zone Transfer (AXFR):


python dns_lookup.py -d example.com -s ns1.example.com --axfr
