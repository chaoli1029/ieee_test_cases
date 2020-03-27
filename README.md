# ieee_test_cases
Classic IEEE test cases for research of reliable unit commitment problem. <br />
There are 3 test cases: 73-bus system, 118-bus system, and Polish system. For each test case, there are data files as follows. <br />

## Data_Size
size of the transmission network <br />
number of buses (N) <br />
number of generators (G) <br />
number of branches (L) <br />
number of periods (T) <br />
number of single-generator-failure scenario (S) <br />

## Data_Branch
attributes of transmission branches <br />
column1: origin bus id <br />
column2: destination bus id <br />
column3: susceptance (for B-theta formulation) <br />
column4: rating A, transmission line capacity <br />
column5: rating C, transmission line capacity post contingency <br />

## Data_Gen
attributes of generators <br />
column1: generator location bus id <br />
column2: generation lower limit <br />
column3: generation upper limit <br />
column4: is must-run unit <br />
column5: is fast ramp-up unit <br />
column6: generation variable cost (p.u.) <br />
column7: commitment start-up cost <br />
column8: commitment no-load cost <br />
column9: commitment minimum up time <br />
column10: commitment minimum down time <br />
column11: hourly ramping limit <br />
column12: start-up ramping limit <br />
column13: shut-down ramping limit <br />
column14: fast ramping limit <br />

## Data_ISF
injection shift factor, also a.k.a. power transfer distribution factor (PTDF), a result of linearization of ACOPF <br />
|N| by |L| matrix, element (n,l): injecting one unit power from bus n, distribution on branch l <br />

## Data_Load
load (i.e., demand) at buses in periods <br />
|N| by |T| matrix, element (n,t): load at bus n in period t <br />

## Data_Scen
single-generator-failure (G-1) contingency scenarios <br />
column1: generator id of the correspond scenario <br />

## Data_Test_Con
crucial extreme ray feasibility cut index tuple (obtained from offline study) <br />
total number of cuts followed by the index tuples (r,s,t), where r maps to the extreme ray id, s maps to the scenario id, and t maps to the period id <br />

## Data_Test_ER
extreme ray characterization (obtained from offline study) <br />
total number of distinct extreme rays followed by the characterization <br />
for each extreme ray: <br />
\tau: scalar <br />
\phi^+: vector of dimension of |G| <br />
\phi^-: vector of dimension of |G| <br />
\lambda: vector of dimension of |N| <br />
\mu^+: vector of dimension of |L| <br />
\mu^-: vector of dimension of |L| <br />
 
## Data_Test_Load
load scenarios for testing (generated from deterministic load) <br />
total number of testing scenarios followed by the load profile <br />
for each testing scenario: <br />
|N| by |T| matrix, element (n,t): load at bus n in period t
