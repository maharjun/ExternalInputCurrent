## Current Description

1.  The random current is a poisson distributed current 
    with 1 Hz Frequency. The Excitation is of amount given by 
	IExtScaleFactor which becomes 0 on the next time step.
	This is done using a variable IExtNeuron, which records
	the neron which received Non-zero current at the particular
	time instant.
	
	This current is in some way, a preliminary version of
	WorkingMemory/Ext-Pattern-and-Random.

## Usage:

It is compatible with all TimeDelNetSim versions which have defined 
the following variables

   StorageStepSize     - Storage Step Size in ms.                              
   beta                - As calculated from Time and StorageStepSize           
   onemsbyTstep        - 1ms/TimeStep (integer)                                
   N                   - Number of Neurons                                     
   NoOfms              - No of ms to simulate for                              
   i                   - Loop Variable.                                        
   Time                - Simulation Time instant as no. of Time Steps since 0 

It is required to be placed in the Headers Directory of Any project so that the 
following files are accessible.

    ..\Network.hpp                                         
    ..\NeuronSim.hpp                                       
    ..\..\..\MexMemoryInterfacing\Headers\MexMem.hpp       
    ..\..\..\MexMemoryInterfacing\Headers\GenericMexIO.hpp 
    ..\..\..\RandomNumGen\Headers\FiltRandomTBB.hpp        

MexMemoryInterfacing Should contain all the generic IO functions. 
Thus it must be any version later than or equal to 

4b3e7b2 BugFix + removed unnecessary undef
