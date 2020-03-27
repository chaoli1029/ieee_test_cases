# ieee_test_cases
Classic IEEE test cases for research of reliable unit commitment problem

# data structure
There are 3 test cases: 73-bus system, 118-bus system, and Polish system.
For each test case, there are data files as follows.

## Data_Size: size of the transmission network
number of buses (N)
number of generators (G)
number of branches (L)
number of periods (T)
number of single-generator-failure scenario (S)

## Data_Branch: attributes of transmission branches
column1: origin bus id
column2: destination bus id
column3: susceptance (for B-theta formulation)
column4: rating A, transmission line capacity
column5: rating C, transmission line capacity post contingency

## Data_Gen: attributes of generators
column1: generator location bus id
column2: generation lower limit
column3: generation upper limit
column4: is must-run unit
column5: is fast ramp-up unit
column6: generation variable cost (p.u.)
column7: commitment start-up cost
column8: commitment no-load cost
column9: commitment minimum up time
column10: commitment minimum down time
column11: hourly ramping limit
column12: start-up ramping limit
column13: shut-down ramping limit
column14: fast ramping limit

## Data_ISF: injection shift factor, also a.k.a. power transfer distribution factor (PTDF), a result of linearization of ACOPF
|N| by |L| matrix
element (n,l): injecting one unit power from bus n, distribution on branch l

## Data_Load: load (i.e., demand) at buses in periods
|N| by |T| matrix
element (n,t): load at bus n in period t

## Data_Scen: single-generator-failure (G-1) contingency scenarios
column1: generator id of the correspond scenario

## Data_Test_Con: crucial extreme ray feasibility cut index tuple (obtained from offline study)
total number of cuts followed by the index tuples (r,s,t), where r maps to the extreme ray id, s maps to the scenario id, and t maps to the period id

## Data_Test_ER: extreme ray characterization (obtained from offline study)
total number of distinct extreme rays followed by the characterization
for each extreme ray:
\tau: scalar
\phi^+: vector of dimension of |G|
\phi^-: vector of dimension of |G|
\lambda: vector of dimension of |N|
\mu^+: vector of dimension of |L|
\mu^-: vector of dimension of |L|
 
## Data_Test_Load: load scenarios for testing (generated from deterministic load)
total number of testing scenarios followed by the load profile
for each testing scenario:
|N| by |T| matrix
element (n,t): load at bus n in period t
