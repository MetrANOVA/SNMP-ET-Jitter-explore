# SNMP-ET-Jitter-explore
This repo contains both scripts and data related to our recent exploration of the impact of poll cycle ET jitter on the accuracy of rate calculations based on time-adjacent samples.

## SNMP-Analysis.ipynb
A Jupyter Notebook script that takes as input a CSV file containing a column of timestamps and IP addresses that correspond to packet captures that record specific bulk requests to a set of routers.
It analyzes the timing and provides the characterization of poll ET Jitter for the set of observed routers and each individual.

## Error-Model.ipynb
A Jupyter Notebook script that attempts to probabilistically estimate total error based on an assumed poll interval and level of Jitter.  This script currently based on a normal distribution where the reported ET Jitter value is used for +- 1 standard deviation.

## snmp-smaller.csv.gz
A compressed CSV that has 2 columns: a timestamp and an integer representing the IP of the router the poller was communicating with.  While mapping each IP to an integer does have the convenient side effect of deidentifying the data, it was mainly done to fit the file in this repository without GitHUB rejecting it.
