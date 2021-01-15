# TaskXDF-monitor
Linux scripts to monitor Einstein@Home Gravitational Wave GPU tasks and AMD card memory usage

These bash scripts are intended for Linux systems running Einstein@Home O2MDF gravitational wave GPU tasks.
Only the following AMD GPUs are supported: Ellesmere, Polaris, Vega, or Navi.

taskXDF-mon-timer is the interval timer script for running the target script, taskXDF-mon.
Place it same folder as taskXDF-mon. The target script can be left as non-executable.
Make sure that the timer script is executable, e.g., ~$ chmod +x taskXDF-mon-timer

Monitored data are: number of running tasks, average task GPU memory requirement and delta frequency values (DFs), and GPU card VRAM and system GTT memory usages. 
Data are written to the Terminal window and to a log file that is created in the parent folder.

General use instructions are provided when the timer script is executed without arguments or with the --help or --about command line arguments. 
For explanation of data reported, use the --header argument.

##Tips:   
Run the timer using a 2 to 5 min interval, e.g., ~$ ./taskXDF-mon-timer 5 .

A time interval of 0 provides a one-off reading. Otherwise, a non-zero interval time provides ongoing readings. 
Executing the taskXDF-mon directly, if it is made executable, can also provide a one-off reading.
