Summary 01: Aircraft travels from **base A to base A** via multiple points in order to do aerial inspections. The route should always be the shortest path while also being able to visit all inspection waypoints.

**Objective:**  
\-\> Visit all inspection waypoints  
\-\> Use the shortest possible path from RPUB to RPUB (Basa Air Base, Pampanga)  
(in codebase this is random due to wartime)

**Variables:**  
**PH waypoints     : 373** //all philippine waypoints inside Manila FIR  
TSP cities (N)   : 55 // selected waypoints

Selected waypoints/cities  
IDENT  LATITUDE  LONGITUDE // detailed positions  
TABUL  6.543503 121.882297  
BAYAN 14.831336 120.655697  
ASTUR 10.617564 123.697572  
SBA65 14.851647 120.391931  
CGO19  8.350422 124.594022  
NOYAN 10.405822 121.004294  
CIA80 15.211369 120.572239  
GARAY 14.912322 121.148872  
SBA23 14.632764 120.008811  
GSA17  6.037708 125.098706  
MUPOB 15.636614 123.054969  
BOHOL  9.571681 124.379603  
KARAG 14.433028 119.945536  
CGO15  8.577431 124.652694  
KAWIT 10.771883 124.504847  
R2683  7.116675 125.635489  
ABLBG 13.843603 120.113717  
MUMOT 19.028583 117.789725  
TALIM 14.356586 121.328114  
DILIS 14.518636 126.001419  
ANKUR  6.658083 121.001386  
MABID  9.995158 124.092969  
CIA16 15.149942 120.693144  
NIBAT  7.464778 125.623447  
PARAL  7.289242 122.261569  
GULFO 10.382100 122.706422  
MINDA 14.468886 120.451564  
MCT20 10.200372 123.937425  
MCT17 10.436000 123.872939  
ZAM64  6.921822 121.952194  
BANGA  6.401264 124.829278  
EDCON 10.195150 123.868781  
BUNGA 11.340331 122.906308  
VICTA 10.974431 123.121356  
RAVIA 10.852786 122.883039  
FLORA  6.904175 122.256650  
CGO67  8.527042 124.595417  
BALAY 13.902681 120.728347  
KAPOH 18.679308 120.569167  
LOPEZ 13.921467 122.202047  
PAKAN  6.485617 125.007678  
SADOK 10.922019 125.310761  
BARBA 11.061269 122.278961  
MIA60 14.523036 121.048519  
EDLOR  6.867217 125.860231  
GSA07  6.192308 125.080353  
DAO50  7.077419 125.589769  
CGO18  8.472553 124.559497  
ALDIS 18.597900 119.663611  
CABRE  9.910125 119.318800  
TEGID  8.948333 115.861667  
JAGIS  9.924122 118.470019  
RAGAY 13.729725 122.584119  
MIA26 14.492281 120.992439  
PALAY  9.994342 122.397636

**Algorithm:**  
**\-\> Hill Climbing**

1. *Start with initial state (Start: Basa Air Base \- Runway 04\)*  
   *cur \= random.sample(range(N), N) \# 1\. initial state line for hc*

   *—-----------------------------------*

   *Explanation: provide initial state via random sample in this case.*

2. *Evaluate all neighboring states (all the PH waypoints above technically)*  
1. *Compute distance between the initial state and the neighboring states(Add the cumulative distance of initial state and neighboring states)*

   *nb\_d \= route\_distance(nb)*

   *Explanation: haversine formula usage for computing distance between states,*

2. *Save distance and output of \[a\], which is the current computed distance*  
3. *Compare the \[a\] to the next \[b\], neighboring state distance (by choosing the shortest distance)*  
4. *Save the shortest distance \[c\] to the variable \[a\].*  
5. *The current distance will be the \[a\]*  
6.  *Repeat comparison (procedures a-e) for all remaining neighboring states*  
3. *Select the best neighbor (the one with the shortest distance) Once we completed all the comparison procedures of all remaining neighboring states*  
     
     
     
   

**Algorithm:**  
**\-\> Genetic Algorithm (non-memetic/memetic)**

**Note: we assume at wartime to introduce fuel measures.**

$$
d = 2R \arcsin \left(
\sqrt{
\sin^2\left(\frac{\phi_2 - \phi_1}{2}\right)
+ \cos(\phi_1)\cos(\phi_2)\sin^2\left(\frac{\lambda_2 - \lambda_1}{2}\right)
}
\right)
$$

Where:

- $R = 6371 \text{ km}$ (Earth's radius)  
- $\phi_1, \phi_2$ = latitudes of the two waypoints (in radians)  
- $\lambda_1, \lambda_2$ = longitudes of the two waypoints (in radians)  
Task:  
Given the formulas above, the task is to do the same exact situation in the Memetic GA as given on the code.

\-\> Algorithm is required.  
\-\> List the parts of the code as well.

Example:

1. Function to eliminate unordered  
   *Increment \- 1;*

Deadline:  Apr 10, 2026