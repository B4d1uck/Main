# Fast Scan
```
# Perform a fast scan on IP addresses listed in the 'scope' file and save the results to 'fast_scan'
sudo nmap -iL scope -F | tee fast_scan
```

1. `sudo`: This command is used to execute the subsequent command (`nmap`) with superuser privileges. It is often required for certain network-related tasks that need elevated permissions.
2. `nmap`: This is the main command. `nmap` is a powerful network scanning tool used to discover hosts and services on a computer network, identifying open ports, and more.
3. `-iL scope`: This option specifies a file (`scope`) containing a list of target IP addresses. the `-iL` flag indicates that it's an input file.
4. `-F`: This flag tells `nmap` to perform a fast scan. It scans only the most common 100 ports for each target, which can significantly reduce the scan time.
5. `|` (***Pipe***): The pipe operator (`|`) is used to pass the output of the `nmap` command as input to the next command (`tee` in this case).
6. `tee fast_scan`: `tee` is a command that reads from standard input and writes to standard output and files simultaneously. In this context, it writes the output of the `nmap` command to a file named `fast_scan` in addition to displaying it on the terminal.

So, in summary, this bash command uses `nmap` to perform a fast scan on a list of IP addresses specified in the file named `scope`. The results are both displayed on the terminal and saved to a file named `fast_scan`. The use of `sudo` indicates that elevated privileges might be needed for certain aspects of the network scan.
