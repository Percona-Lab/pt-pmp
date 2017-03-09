# pt-pmp

pt-pmp is a poor man's profiler, inspired by <http://poormansprofiler.org>.
It can create and summarize full stack traces of processes on Linux.
Summaries of stack traces can be an invaluable tool for diagnosing what
a process is waiting for.

This version of pt-pmp has a several enchantments that for the moment are not 
integrated into main pt-pmp tool(https://github.com/percona/percona-toolkit)

= support of the several tools that produces stack traces:

New option: -d gdb|eu|pteu|qs

GDB                   -> pt-pmp -d gdb 
eu-stack(elfutils)    -> pt-pmp -d eu
pt-eustack-resolver   -> pt-pmp -d pteu
quickstack            -> pt-pmp -d qs

pt-eustack-resolver - tool for offline symbol resoving of traces obtained
with eu-stack

=  possibility to filter out stack traces only for specific tids

New option: -t tid[,tid,tid,...]



