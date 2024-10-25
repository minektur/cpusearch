# cpusearch
CLI utility to fuzzy search and scrape data about CPUs off cpubenchmark.net (benchmark, cores, tdp, socket, etc)

## why?
You ever go trolling ebay for used computer junk and want to understand the relative computing power of 
some device you're going to buy?  Is this random computer a good deal for the relative computing power
it has?  How much power is this system likely to consume, relative to some other one?  Or, if I wanted to upgrade
cpus for some system I have, would this one work?  How much more power would it use?  Is this slightly older
server more or less powerful than that other one there?  I'm not saying I spend a lot of time window shopping 
like this, but well, I do.

## what?
This very-hacky script google searches the cpu terms you give on the command line and then finds that on
cpubenchmarks.net.  It then scrapes a bunch of data about that cpu and prints it out in a single line.

It's not clean code, but it works.

#examples

    $ cpusearch Xeon® processor D-1537
    ('Intel Xeon D-1537 @ 1.70GHz', ['7444', '1225'], 'Cores: 8 Threads: 16', 'FCBGA1667', '35 W', 'CPUmark/$Price: 13.04')

    $ cpusearch gold 6230
    ('Intel Xeon Gold 6230 @ 2.10GHz', ['27069', '2269'], 'Cores: 20 Threads: 40', 'FCLGA3647', '125 W', 'CPUmark/$Price: 32.46')

    $ cpusearch platinum 8580
    ('Intel Xeon Platinum 8592+', ['84013', '2411'], 'Cores: 64 Threads: 128', 'FCLGA4677', '350 W', 'CPUmark/$Price: 7.24')

    $ cpusearch e5 2407 v2
    ('Intel Xeon E5-2407 v2 @ 2.40GHz', ['3504', '1068'], 'Cores: 4 Threads: 4', 'FCLGA1356', '80 W', 'CPUmark/$Price: 86.53')

