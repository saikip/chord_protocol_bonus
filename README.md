## **CHORD PROTOCOL (BONUS) - COP5615: Fall 2018**

## **TEAM INFO**
Priyam Saikia (UFID **** ****)

## **PROBLEM**
Implement failure model for the chord protocol that was designed using 
genserver/Actor model in Elixir based on the Chord MIT paper.

## **INSTALLATION AND RUN** 

Elixir Mix project is required to be installed. 

Files of importance in the zipped folder (in order of call):

*entrypoint.exs*     -> Commandline entry module

*chord_protocol.ex*  -> Main Module

*supervisor.ex*     -> Supervisor Module

*chord_boss.ex*      -> Worker Module

*Node_join.ex*       -> Sub-Module for join and stabilize

To run a test case, do:

1. Unzip contents to your desired elixir project folder.
2. Open cmd window from this project location (use $cd <location> to change location)
3. Type "mix run entrypoint.exs <numNodes> <numRequests> <failNodes>" in commandline without quotes. 
4. The run terminates when all the peers perform given number of requests (details in report). 
5. The result provides the average number of hops for the message to be delivered

Example:
	C:\Users\PSaikia\Documents\Elixir\kv\chord_protocol_bonus>mix run entrypoint.exs 1000 10 10
	
	Chord Protocol begins...
	
	Average hops: 4.863500000000002
	
	Completed Chord Protocol
   
## **WHAT IS WORKING**

We have implemented the failure model for the Chord Protocol as mentioned on the Section 5 
of the given paper. We check the resiliency of our protocol after implementation of this 
failure model. Our failure model works as and can be verified by the output number of hops.
As the number of failed nodes increase, the number of hops increases too. So, it takes more
time to reach the destination but the model is resilient. More details of the implementation
is detailed in the report.

## **LARGEST NETWORK**
    
**Largest network tested** (for percent of failed nodes = 10%): 
	
	Largest Number of Nodes tested: 5000
	
	Largest Number of Requests: 100
	
Sample:
	
	C:\Users\PSaikia\Documents\Elixir\kv\chord_protocol_bonus>mix run entrypoint.exs 5000 100 10
	
	Chord Protocol begins...
	
	Average hops: 5.1703920000000023
	
	Completed Chord Protocol
