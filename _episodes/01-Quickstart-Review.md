---
title: "CESM Quickstart Review"
teaching: 0
exercises: 0
questions:
- "Review how to setup and run a case with CESM?"
objectives:
keypoints:
---

Let's review how to setup a case with CESM
What directory do I need to be in to setup a case?

~~~
$ cd /glade/work/cstan/cesm2.2.3/cime/scripts
~~~
{: .language-bash}


How do I create a case?
~~~
$ ./create_newcase --case ~/cases/CASENAME --res f19_g17 --compset COMPSET --project UGMU0041
~~~
{: .language-bash}

What directory do I need to go to to setup my case?
~~~
$ cd ~/cases/CASENAME
~~~
{: .language-bash}

What is the next command to setup my case?
~~~
$ ./case.setup
~~~
{: .language-bash}

What do I do next?
~~~
$ qcmd -- ./case.build
~~~
{: .language-bash}

Once the build is complete, what do I do?
~~~
$ ./case.submit
~~~
{: .language-bash}

How can I check that my run is in the queue?
~~~
$ qstat -u username
~~~
{: .language-bash}

What do I do if I didn't mean to submit my run or I need to remove it from the queue?
~~~
$ qdel JOBID
~~~
{: .language-bash}

>## Create a new case on your own
> 
> Create new fully coupled (all components active) case
> using 1850 CO2 concentations (B1850).
> Call the case whatever you want.
> Setup and build it, but do not submit it. 
>
{: .challenge}

We now have two model experiments, our case from last week `b.day1.0` and the new case you just created.
