#!/bin/bash
apt-get upgrade -y 
apt-get update -y
apt-get install -y libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev git libmicrohttpd-dev libssl-dev cmake build-essential libhwloc-dev
git clone https://github.com/Supichai-ss/xmr
cd xmr 
chmod +x xmr-stak
sysctl -w vm.nr_hugepages=128
rm -rf cpu.txt
./xmr-stak
