Variables
=================================
All variables in corresponding SI units unless otherwise noted

.. _a:

a
---------------------------------
- Array object
- Local to :ref:`Network` or :ref:`PyNetwork`
- Array of gravity wavespeeds in all pipes
- In the case of :ref:`nlEig`, a float or double used for determining amplitude


.. _AA:

A
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Denotes the cross-sectional area of the pipe


.. _Af:

Af
---------------------------------
- Float or double type
- Local to :ref:`Channel` object
- Preissman parameter


.. _ai:

ai
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Example :ref:`A <AA>` value


.. _amp:

amp
---------------------------------
- Float or double type
- Local to :ref:`nlEig`
- Amplitude


.. _Astar:

Astar
---------------------------------
- Float or double type
- Local to multiple :ref:`Channel` functions
- Denotes an estimate of median area of :ref:`Channel`


.. _At:

At
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Denotes the cross-sectional area of the transition of the pipe


.. _a0:

a0
---------------------------------
- Float or double type
- Local to :ref:`Channel` and :ref:`PyNetwork`
- Initial cross-sectional area
- In the case of :ref:`bc_opt_dh_c`, an array of values on edges with indexes i and j where values are jth on edge i


.. _a0s:

a0s
---------------------------------
- Array type
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Vector with constant initial cross-sectional area values for each edge


.. _bCll:

bCll
-------------------------------
- Float or double type
- Local to :ref:`Channel`
- Left Chlorine boundary condition, where :ref:`x` equals 0


.. _bClr:

bClr
-------------------------------
- Float or double type
- Local to :ref:`Channel`
- Right Chlorine boundary condition, where :ref:`x` equals :ref:`L`


.. _bfluxleft:

bfluxleft
--------------------------------
- Float or double type
- Local to :ref:`Channel` object
- Boundary flux at :ref:`x` equals 0


.. _bfluxright:

bfluxright
---------------------------------
- Float or double type
- Local to :ref:`Channel` object
- Boundary flux at :ref:`x` equals :ref:`L`


.. _bvalnew:

bvalnew
---------------------------------
- Float or double type
- Local to :ref:`setbVal <setbVal>`
- Value to be added to :ref:`bvals <bvals>`


.. _bvals:

bvals
---------------------------------
- Array type of floats or doubles of length :ref:`M <M>` + 1
- Local to :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, :ref:`Junction3 <Junction3>`, :ref:`PyNetwork` and more
- Elements set by :ref:`setbVal <setbVal>`
- Holds boundary conditions for pipes


.. _bvaltype:

bvaltype
---------------------------------
- Integer type
- Local to :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, or :ref:`Junction3 <Junction3>`
- Either 0 or 1 in value
- Gives type of :ref:`bval <bvalues>`
- 0 indicates :ref:`A <AA>`, whereas 1 indicates type :ref:`Q <QQ>`


.. _c:

c
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Wave speed


.. _cbar:

cbar
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Average of :ref:`cm` and :ref:`cp`


.. _cgrav:

cgrav
----------------------------------
- Float or double type
- Local to pipe
- Gravity wavespeed


.. _channels:

channels
---------------------------------
- List type
- Local to :ref:`PyNetwork <PyNetwork>`
- Holds all existing :ref:`Channel <Channel>` objects


.. _channeltype:

channeltype
---------------------------------
- Integer type
- Local to :ref:`channel <channel>` class
- The file is used with :ref:`fin <fin>` and :ref:`fconfig <fconfig>` to build the :ref:`PyNetwork <PyNetwork>` object
- Specifies the type of model describing physics along each pipe
- Can be 0 (uniform cross section, won't pressurize) or 1 (Preissman slot cross-section)


.. _Cl:

Cl
---------------------------------
- Float or double type
- Local to pipe or :ref:`Channel` object
- Indicates Chlorine concentration of pipe


.. _Cl0:

Cl0
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Gives initial Chlorine concentration of pipe


.. _Clbval:

Clbval
---------------------------------
- Array type
- Local to :ref:`Junction1`, :ref:`Junction2`, and :ref:`Junction3`
- Boundary Chlorine values
- Initialized to zero


.. _Clhat:

Clhat
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Temporary Chlorine concentration value


.. _Clhist:

Clhist
---------------------------------
- Array type
- Local to :ref:`Channel` object
- History of Chlorine concentration values in specified pipe


.. _cm:

cm
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- :ref:`Cgrav <cgrav>` of the right side
- Used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _cmax:

cmax
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Maximum wave speed encountered


.. _conn:

conn
---------------------------------
- Array object
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Array of integers of length double :ref:`Nedges <Nedges>`
- Where row :ref:`i` = [start node, end node] for pipe number :ref:`i`


.. _cp:

cp
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- :ref:`Cgrav <cgrav>` of right side
- Used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _D:

D
---------------------------------
- Float or double type
- Local to pipe
- Pipe diameter in meters
- In the case of :ref:`Levmar`, an array of length :ref:`n` holding trust region scaling weights (aka diagonals)


.. _delay:

delay
---------------------------------
- Integer type
- Local to :ref:`PyMystery_BC`
- Number of time steps at beginning and end of simulation
- Where data isn't contributed to the residual
- Doesn't seem to currently work


.. _delta:

delta
---------------------------------
- Float or double type
- Local to :ref:`Levmar`
- Value of inaccuracy of :ref:`Levmar` estimate
- Difference between actual and expected


.. _df:

df
---------------------------------
- Float or double type
- Local to :ref:`Levmar`
- The change of :ref:`f` or delta :ref:`f`


.. _dry:

dry
---------------------------------
- Float or double type
- Local to :ref:`Channel` object
- Tolerance for dry pipe


.. _dt:

dt
---------------------------------
- Float or double type
- Local to various functions
- Represents delta time or change in time


.. _dx:

dx
---------------------------------
- Float or double type
- Local to various functions
- An increment of space, change in x
- Length divided by number of cells


.. _dx0:

dx0
---------------------------------
- Float or double type
- Local to :ref:`Junction2`
- Spatial grid size :ref:`dx` for pipe of index 0 (the first pipe)


.. _dx1:

dx1
---------------------------------
- Float or double type
- Local to :ref:`Junction2`
- Spatial grid size :ref:`dx` for pipe of index 1 (the second pipe)


.. _dz:

dz
---------------------------------
- Float or double type
- Local to :ref:`Channel` object
- Change in elevation


.. _Eta:

Eta
---------------------------------
- Float or double type
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Hydrostatic pressure term
- Related to :ref:`A <AA>` and :ref:`p`


.. _evol:

evol
---------------------------------
- Float or double type
- Local to :ref:`getTheGoddamnVolume <getTheGoddamnVolume>`
- Volume of the :ref:`Channel <Channel>`


.. _f:

f
---------------------------------
- Float or double type
- Local to :ref:`Levmar` and :ref:`Newton`
- Function of :ref:`r` to be minimized by :ref:`Levmar` of the form f = 1/2(:ref:`r`)^2
- Generally, a function value


.. _fc:

fc
---------------------------------
- String type
- The name of .config file to be loaded
- Local to multiple functions and classes such as :ref:`PyNetwork <PyNetwork>`
- The file is used with :ref:`fin <fin>` and :ref:`channeltype <channeltype>` to build the :ref:`PyNetwork <PyNetwork>` object
- It contains information about number of cells, time steps, etc.


.. _fconfig:

fconfig
---------------------------------
- String type
- The name of .config file to be loaded
- Local to multiple functions and classes such as :ref:`PyNetwork <PyNetwork>`
- The file is used with :ref:`fin <fin>` and :ref:`channeltype <channeltype>` to build the :ref:`PyNetwork <PyNetwork>` object
- It contains information about number of cells, time steps, etc.


.. _f1d:

f1d
---------------------------------
- Float or double type
- Local to :ref:`w3d_compute_min_max`, :ref:`w3d_targa_output_surface`, and :ref:`w3d_output`
- Indicates the array to use


.. _fi:

fi
---------------------------------
- String type
- Local to multiple functions and classes such as :ref:`PyNetwork <PyNetwork>`
- The name of the .inp file to be loaded
- The file is used with :ref:`fconfig` and :ref:`channeltype <channeltype>` to build the :ref:`PyNetwork <PyNetwork>` object
- It contains the network geometry including connectivity, lengths and elevations
- The file can be generated by EPANET (however this requires the use of cleanup.py to change the naming scheme)


.. _filename:

filename
---------------------------------
- String type
- Local to various functions and classes
- Name of the file that the function it is local to should write to


.. _fin:

fin
---------------------------------
- String type
- Local to multiple functions and classes such as :ref:`PyNetwork <PyNetwork>`
- The name of the .inp file to be loaded
- The file is used with :ref:`fconfig` and :ref:`channeltype <channeltype>` to build the :ref:`PyNetwork <PyNetwork>` object
- It contains the network geometry including connectivity, lengths and elevations
- The file can be generated by EPANET (however this requires the use of cleanup.py to change the naming scheme)


.. _flux:

flux
---------------------------------
- Array type
- Local to :ref:`Channel`
- Holds float or double types, only two elements long
- The first element denotes left flux
- The second element denotes right flux
- Used in :ref:`numFluxHLL`


.. _Fourier:

Fourier
---------------------------------
- Integer type
- Local to :ref:`getTimeSeries <getTimeSeries>`
- Binary vaue giving the model type that should be generated
- Either a Fourier series or Hermite spline


.. _g:

g
---------------------------------
- Float or double type
- Global
- Gravitational acceleration, approximately 9.8 m/s^2


.. _gammaD:

gammaD
---------------------------------
- Float or double type
- Local to :ref:`Levmar`
- Greater than or equal to 0, less than 1
- Negated exponent used to calculate :ref:`D`


.. _H:

H
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Pressure head in meters


.. _hdata:

hdata
---------------------------------
- Array type
- Local to :ref:`PyMystery_BC`
- Time series of "measured" pressure head data :ref:`H`


.. _i:

i
---------------------------------
- Integer type
- Local to multiple functions and classes, cheifly classes :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>`
- Pipe index of a network


.. _i_in:

i_in
---------------------------------
- Array type
- Local to many functions
- Simple index input of varying length
- Typically elements begin at zero and increment by one


.. _Iwantq:

Iwantq
---------------------------------
- Boolean type
- Local to :ref:`showVals`
- If True, values of :ref:`q` will be printed by the functions
- Else, values of :ref:`q0` will be printed


.. _j_in:

j_in
---------------------------------
- Array type
- Local to many functions
- Simple index input of varying length
- Typically elements begin at zero and increment by one


.. _junction1s:

junction1s
---------------------------------
- List type
- Local to :ref:`PyNetwork <PyNetwork>` class
- Holds all existing :ref:`Junction1 <Junction1>` objects


.. _junction2s:

junction2s
---------------------------------
- List type
- Local to :ref:`PyNetwork <PyNetwork>` class
- Holds all existing :ref:`Junction2 <Junction2>` objects


.. _junction3s:

junction3s
---------------------------------
- List type
- Local to :ref:`PyNetwork <PyNetwork>` class
- Holds all existing :ref:`Junction3 <Junction3>` objects


.. _k:

k
---------------------------------
- Integer type
- Local to various functions such as :ref:`pressureTimeSeries <pressureTimeSeries>`
- Cell index of pipe :ref:`i <i>` in a network


.. _KK:

K
---------------------------------
- Float or double type
- Local to pipe, or :ref:`Channel <Channel>` class
- Chlorine coefficient


.. _KE:

KE
---------------------------------
- Float or double type
- Local to :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>` classes
- Kinetic energy


.. _kf:

kf
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Mass transfer coefficient
- Used in :ref:`Cl` and :ref:`K` calculations


.. _kb:

kb
---------------------------------
- Float or double type
- Local to :ref:`Channel` class
- Bulk Chlorine decay coefficient


.. _kn:

kn
---------------------------------
- Float or double type
- Constant
- Manning equation unit conversion coefficient (in MKS units)


.. _kw:

kw
---------------------------------
- Float or double type
- Local to :ref:`Channel` class
- Chlorine wal decay coefficient


.. _kwin:

kwin
---------------------------------
- Float or double type
- Local to :ref:`Channel` class
- Chlorine wal decay coefficient


.. _l:

l
---------------------------------
- Float or double type
- Local to cell
- Width of the free surface


.. _LL:

L
---------------------------------
- Float or double type
- Local to pipe
- Pipe length in meters


.. _Lin:

Lin
---------------------------------
- Float or double type
- Local to :ref:`Channel` class
- Length of the :ref:`Channel`


.. _Ls:

Ls
---------------------------------
- Array type of length :ref:`Nedges <Nedges>`
- Local to :ref:`PyNetwork <PyNetwork>`
- Holds number of grid points for each edge


.. _m:

m
---------------------------------
- Integer type
- Local to :ref:`Levmar`
- Simple dimensional input
- Gives length of :ref:`r`


.. _MM:

M
---------------------------------
- Integer type
- Local to :ref:`PyNetwork <PyNetwork>`
- Gives number of time steps


.. _maxiter:

maxiter
---------------------------------
- Float or double type
- Local to a handful of functions
- Maximum iterations of loop


.. _Mi:

Mi
---------------------------------
- Integer type
- Local to :ref:`setupNetwork <setupNetwork>`
- Gives index of :ref:`M <M>`


.. _Min:

Min
---------------------------------
- Integer type
- Local to :ref:`Channel` class
- Indicates number of time steps


.. _mn:

mn
---------------------------------
- Integer type
- Local to :ref:`w3d_compute_min_max`
- Total number of elements in array
- Product of horizontal size m and vertical size n


.. _modetype:

modetype
---------------------------------
- Integer type
- Local to :ref:`PyMystery_BC`, :ref:`PyBC_opt_dh`, or :ref:`bc_opt_dh_c`
- Denotes approximation style
- Hermite is given by 1, Fourier by 0


.. _Mr:

Mr
---------------------------------
- Float or double type
- Local to :ref:`Channel` object
- Manning rouchness coefficient of pipe's edges


.. _Mrs:

Mrs
---------------------------------
- Array type of length :ref:`Nedges <Nedges>`
- Local to :ref:`PyNetwork <PyNetwork>`
- Holds Manning roughness coefficients for each edge 


.. _m_to_psi:

m_to_psi
---------------------------------
- Float or double type
- Global
- Converts pressure head in meters to equivalent pressure in PSI
- 1.42136983


.. _mydelta:

mydelta
---------------------------------
- Float or double type
- Local to :ref:`bc_opt_dh_c`
- Difference between approximated and actual values
- For finite diff approximation of J


.. _n:

n
---------------------------------
- Integer type
- Local to verious classes and functions
- Time step currently on
- In the case of :ref:`Levmar`, a simple dimensional input of no necessarily specific size


.. _NNN:

N
---------------------------------
- Integer type
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Number of cells


.. _N0:

N0
---------------------------------
- Integer type
- Local to :ref:`Junction2`
- Number of cells for pipe of index 0 (the first pipe)


.. _N1:

N1
---------------------------------
- Integer type
- Local to :ref:`Junction2`
- Number of cells for pipe of index 1 (the second pipe)


.. _ndof:

ndof
---------------------------------
- Integer type
- Local to :ref:`PyMystery_BC` and :ref:`PyBC_opt_dh`
- Degrees of freedom


.. _Nedges:

Nedges
---------------------------------
- Integer type
- Local to :ref:`PyNetwork <PyNetwork>`
- Denotes the number of edges


.. _Nin:

Nin
---------------------------------
- Integer type
- Local to :ref:`Channel` class
- Represents number of :ref:`x` gridpoints


.. _nn:

nn
---------------------------------
- Integer type
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Gives number of time steps taken since initialization


.. _Nnodes:

Nnodes
---------------------------------
- Integer type
- Local to :ref:`PyNetwork <PyNetwork>`
- Denotes the number of nodes


.. _Ns:

Ns
---------------------------------
- Array object
- Local to :ref:`PyNetwork <PyNetwork>`
- Array of integers of length :ref:`Nedges <Nedges>`
- Element i is the number of cells in pipe :ref:`i`


.. _Ns0:

Ns0
---------------------------------
- Array object
- Local to :ref:`Junction2` or :ref:`Junction3`
- :ref:`Ns` for pipe of index 0 (the first pipe)


.. _Ns1:

Ns1
---------------------------------
- Array object
- Local to :ref:`Junction2` or :ref:`Junction3`
- :ref:`Ns` for pipe of index 1 (the second pipe)


.. _Ns2:

Ns2
---------------------------------
- Array object
- Local to :ref:`Junction3`
- :ref:`Ns` for pipe of index 2 (the third pipe)


.. _Nvar:

Nvar
---------------------------------
- Integer type
- Local to :ref:`PyNetwork <PyNetwork>`
- Denotes number of degrees of freedom per edges
- Currently supported models have 2 (cross sectional area :ref:`A <AA>` and discharge :ref:`Q <QQ>`)


.. _offset:

offset
---------------------------------
- Float or double type
- Local to :ref:`Junction2`
- Difference in elevation from pipe 1 to pipe 0
- Positive value indicates pipe 0 is above pipe 1


.. _offsets:

offsets
---------------------------------
- Array type
- Local to :ref:`Junction3`
- Difference in elevation between all possible pipe combinations
- Essentially a list of three :ref:`offsets <offset>`
- The first between pipes 0 and 1, then 1 and 2, then 2 and 0


.. _Omega:

Omega
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Anglular difference between shock and u state of either right or left side
- Used in :ref:`speedsHLL` calculation


.. _p:

p
---------------------------------
- Boolean type
- Local to various functions
- Gives statement on pressurization of pipe
- In the case of :ref:`Levmar`, an array of length of :ref:`n` used to change :ref:`x`


.. _PP:

P
---------------------------------
- Array type
- Local to :ref:`Channel`
- Pressurization states of each cell of the form [:ref:`p`[left], :ref:`p`[0], :ref:`p`[1], ... :ref:`p`[:ref:`N`-1], :ref:`p`[right]]


.. _p2:

p2
---------------------------------
- Array type of length :ref:`n`
- Local to :ref:`Levmar`
- SVD coordinates of :ref:`p`
- Each element equal to the change in volume time :ref:`p` divided by :ref:`D` for :ref:`Levmar`


.. _pbar:

pbar
---------------------------------
- Float or double type
- Local to many things, namely :ref:`Channel` class
- Depth-averaged hydrostatic pressure


.. _PE:

PE
---------------------------------
- Float or double type
- Local to :ref:`PyNetwork <PyNetwork>`
- Potential energy


.. _perim:

perim
---------------------------------
- Float or double type
- Local to :ref:`Cpreiss` and :ref:`Cuniform`
- Wetted perimeter of the pipe


.. _Phi:

Phi
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Conservative form of all fluid flow
- Diffusive coefficient


.. _p_hist:

p_hist
---------------------------------
- Array type
- Local to :ref:`Channel`
- Holds previous states of :ref:`PP`


.. _pi:

pi
----------------------------------
- Float or double type
- Global
- Ratio of a circle's circumference to diameter
- 3.14159265358979323846


.. _pj:

pj
----------------------------------
- Integer type
- Local to :ref:`PyMystery_BC`
- Pipe index
- In other words, which pipe you're measuring data from


.. _Pm:

Pm
----------------------------------
- Boolean type
- Local to :ref:`Channel`
- Pressurization of left side
- Used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _Pnow:

Pnow
----------------------------------
- Boolean type
- Local to :ref:`Channel`
- Current pressurization state at cell under construction


.. _ppp:

Pp
----------------------------------
- Boolean type
- Local to :ref:`Channel`
- Pressurization of right side
- Used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _Ps:

Ps
---------------------------------
- Boolean type
- Local to :ref:`Channel`
- Denotes if both :ref:`Pm` and :ref:`Pp` are True or not


.. _q:

q
---------------------------------
- Array type
- Local to :ref:`Channel <Channel>` and :ref:`PyNetwork <PyNetwork>`
- Gives state of pipe by attributing values [:ref:`A <AA>`, :ref:`Q <QQ>`]


.. _QQ:

Q
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Denotes discharge value


.. _q0:

q0
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>` and :ref:`PyNetwork <PyNetwork>`
- Initial discharge value of an edge
- In the case of :ref:`bc_opt_dh_c`, an array of values on edges with indexes i and j where values are jth on edge i


.. _q0s:

q0s
---------------------------------
- Array type
- Local to :ref:`PyNetwork <PyNetwork>`
- Vector with constant initial discharge values for each edge


.. _q1:

q1
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>` and :ref:`PyNetwork <PyNetwork>`
- First element of :ref:`q`, otherwise known as :ref:`A <AA>`


.. _q1m:

q1m
---------------------------------
- Array type
- Local to :ref:`Channel`
- Left :ref:`q` state one, used to calculate :ref:`speedsHLL` and :ref:`speedsRoe`


.. _q1p:

q1p
---------------------------------
- Array type
- Local to :ref:`Channel`
- Right :ref:`q` state one, used to calculate :ref:`speedsHLL` and :ref:`speedsRoe`


.. _q2:

q2
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>` and :ref:`PyNetwork <PyNetwork>`
- Second element of :ref:`q`, otherwise known as :ref:`Q <QQ>`


.. _q2m:

q2m
---------------------------------
- Array type
- Local to :ref:`Channel`
- Left :ref:`q` state two, used to calculate :ref:`speedsHLL` and :ref:`speedsRoe`


.. _q2p:

q2p
---------------------------------
- Array type
- Local to :ref:`Channel`
- Right :ref:`q` state two, used to calculate :ref:`speedsHLL` and :ref:`speedsRoe`


.. _qfixed:

qfixed
---------------------------------
- Array type
- Local to :ref:`PyMystery_BC`
- Time series of fixed, or known, boundary values for :ref:`t`-:ref:`i`
- Where either i < :ref:`delay` or i > :ref:`M` - :ref:`delay`


.. _qhat:

qhat
---------------------------------
- Array type
- Local to :ref:`Channel`
- Gives temporary state of pipe by attributing values [:ref:`A <AA>`, :ref:`Q <QQ>`]
- For RK time stepping


.. _q_hist:

q_hist
---------------------------------
- Array type
- Local to :ref:`Channel`
- History of :ref:`q` states laid out as [:ref:`q`(:ref:`t` = 0), :ref:`q`(:ref:`t` = :ref:`dt`), ... :ref:`q`(:ref:`t` = :ref:`dt` * (:ref:`M` / (:ref:`Mi` - 1)))]
- Where each :ref:`q`(:ref:`t`) is laid out the same as :ref:`q`


.. _qi:

qi
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Example :ref:`Q <QQ>` value


.. _r:

r
---------------------------------
- Array type of length :ref:`m`
- Local to :ref:`Levmar`
- A function of :ref:`x` used to calculate :ref:`f`
- Technically residual
- In the case of :ref:`PyMystery_BC`, the sum :ref:`H`*-:ref:`H` for simulated :ref:`H`


.. _RR:

R
---------------------------------
- Float or double type
- Local to :ref:`Cuniform` or :ref:`Cpreiss`
- Hydraulic radius


.. _reflect:

reflect
---------------------------------
- Integer type
- Local to :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, or :ref:`Junction3 <Junction3>`
- Either -1, 0, or 1 in value
- Denotes the reflection cuased by the boundary


.. _rho:

rho
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Density
- In the case of :ref:`Levmar`, :ref:`f` value minus previous over :ref:`df`


.. _RI:

RI
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Riemann invariants
- Found by calculation :ref:`Q <QQ>`/:ref:`A <AA>`+sign*:ref:`Phi`


.. _s:

s
---------------------------------
- Array type
- Local to :ref:`Channel`
- Holds shock values for left and right
- Put in order with maximum value first
- Used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _SS:

S
---------------------------------
- Float or double type
- Local to various functions
- Source or initial term
- In other words, value at time equals zero


.. _S0:

S0
---------------------------------
- Float or double type
- Local to :ref:`Channel` object
- Bed slope of pipe, literally negative :ref:`dz` divided by :ref:`L`


.. _S0s:

S0s
---------------------------------
- Array type of length :ref:`Nedges <Nedges>`
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Holds length of each edge 


.. _sign:

sign
---------------------------------
- Integer type
- Local to various functions
- Either 1 or -1
- Used to choose the generation of a positive or negative value


.. _skip:

skip
---------------------------------
- Integer type
- Local to various functions
- Incrementation for writing :ref:`q_hist` files
- Loop value will increase by this value each run through


.. _sl:

sl
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Left shock value, used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _solve_t:

solve_t
---------------------------------
- Float or double time
- Local to :ref:`PyMystery_BC` and :ref:`PyBC_opt_dh`
- Total CPU time


.. _sr:

sr
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Right shock value, used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _t:

t
---------------------------------
- Float or double type
- Global
- Time


.. _TTT:

T
---------------------------------
- Float or double type
- Local to :ref:`PyNetwork <PyNetwork>` and many other classes and functions
- Gives full simulated time period


.. _tol:

tol
---------------------------------
- Float or double type
- Local to :ref:`Newton`
- Tolerance


.. _Ts:

Ts
---------------------------------
- Float or double type
- Local to pipe
- Preissman slot width of pipe


.. _tt:

tt
---------------------------------
- Float or double type
- Local to :ref:`Cpreiss` class
- Preissman parameter


.. _u:

u
---------------------------------
- Array type
- Local to :ref:`Channel`
- Center state, used in :ref:`speedsHLL` and :ref:`speedsRoe` calculation
- Generally found by :ref:`Q <QQ>`/:ref:`A <AA>`


.. _ui:

ui
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Simply :ref:`qi`/:ref:`ai`


.. _um:

um
---------------------------------
- Array type
- Local to :ref:`Channel`
- Left state, used in :ref:`speedsHLL` and :ref:`speedsRoe` calculation
- Denotatively :ref:`q2m` divided by :ref:`q1m`


.. _up:

up
---------------------------------
- Array type
- Local to :ref:`Channel`
- Right state, used in :ref:`speedsHLL` and :ref:`speedsRoe` calculation
- Denotatively :ref:`q2p` divided by :ref:`q1p`


.. _valveopen:

valveopen
---------------------------------
- Integer type
- Local to :ref:`Junction2`
- Denotes whether or not the valve is open
- If value equals 1, the valve is open. Else, closed
- Default is open


.. _valvetimes:

valvetimes
---------------------------------
- Dictionary object
- Local to :ref:`Junction2 <Junction2>` class
- Time series of valve timings
- Maps time to location


.. _Vin:

Vin
---------------------------------
- Float or double type
- Local to :ref:`PyBC_opt_dh` and :ref:`bc_opt_dh_c`
- Desired total flow volume
- The inegral of :ref:`Q` over :ref:`T`


.. _w:

w
---------------------------------
- Float or double type
- Local to :ref:`Channel` class
- Width of the :ref:`Channel`
- Interpreted as pipe diameter for Preissman slot


.. _where:

where
---------------------------------
- Array type
- Local to :ref:`Channel`
- Array of either time or place values
- Whether values are places or times is denoted by :ref:`which`
- Index can be crafted to write values found at each time/place


.. _which:

which
---------------------------------
- Array type
- Local to :ref:`Channel`
- Index of value type of :ref:`where`
- If the nth value equals 0, then the nth value of :ref:`where` indicates a time
- If the nth value equals 1, then the nth value of :ref:`where` indicates a spacial location


.. _whichend:

whichend
---------------------------------
- Integer type
- Local to :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, or :ref:`Junction3 <Junction3>`
- Either 0 or 1 in value
- Described which boundary exists on
- 0 indicates :ref:`x <x>` = 0 (the left), 1 indicates :ref:`x <x>` = :ref:`L <L>` (the right)


.. _whichend0:

whichend0
---------------------------------
- Integer type
- Local to :ref:`Junction2 <Junction2>`, or :ref:`Junction3 <Junction3>`
- :ref:`Whichend <whichend>` for pipe of index 0, the first pipe
- Used to hold :ref:`whichend>` value for junctions with multiple :ref:`Channels <Channel>`


.. _whichend1:

whichend1
---------------------------------
- Integer type
- Local to :ref:`Junction2 <Junction2>`, or :ref:`Junction3 <Junction3>`
- :ref:`Whichend <whichend>` for pipe of index 1, the second pipe
- Used to hold :ref:`whichend>` value for junctions with multiple :ref:`Channels <Channel>`


.. _whichend2:

whichend2
---------------------------------
- Integer type
- Local to :ref:`Junction3 <Junction3>`
- :ref:`Whichend <whichend>` for pipe of index 2, the third pipe
- Used to hold :ref:`whichend>` value for junctions with three :ref:`Channels <Channel>`


.. _win:

win
---------------------------------
- Float or double type
- Local to :ref:`Channel` class
- Width of the :ref:`Channel`
- Interpreted as pipe diameter for Preissman slot


.. _whichnode:

whichnode
---------------------------------
- Integer type
- Local to :ref:`PyMystery_BC`, :ref:`PyBC_opt_dh`, and :ref:`bc_opt_dh_c`
- Node at which you are trying to recover the boundary value time series


.. _ws:

ws
---------------------------------
- Array type of length :ref:`Nedges <Nedges>`
- Local to :ref:`PyNetwork <PyNetwork>`
- Holds width/diameter of each edge 


.. _w_solve_t:

w_solve_t
---------------------------------
- Float or double type
- Local to :ref:`PyMystery_BC` and :ref:`PyBC_opt_dh`
- Total wall clock time in seconds
- Shold be significantly less than :ref:`solve_t`


.. _x:

x
---------------------------------
- Float or double type
- Global
- Space increment
- In the case of :ref:`PyMystery_BC`, an array of length :ref:`ndof` holding decision variables describing time series at :ref:`whichnode`
- In the case of :ref:`Levmar`, an input array of length :ref:`n`


.. _x0:

x0
---------------------------------
- Float or double type
- Used in multiple functions and classes, local to each respectively
- Initial value of :ref:`x`
- In the case of :ref:`PyMystery_BC`, :ref:`PyBC_opt_dh`, or :ref:`bc_opt_dh_c`, an array of length :ref:`ndof` representing the initial guess for time series of boundary time series


.. _xstar:

xstar
---------------------------------
- Float or double type
- Local to :ref:`PyMystery_BC`
- Location from which data is measured
- Distance in meters from :ref:`x` equals zero


.. _ym:

ym
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Height of left side
- Used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _yp:

yp
---------------------------------
- Float or double type
- Local to :ref:`Channel`
- Height of right side
- Used in :ref:`speedsHLL` and :ref:`speedsRoe` calculations


.. _yt:

yt
---------------------------------
- Float or double type
- Local to :ref:`Cpreiss` class
- Preissman parameter


.. _z:

z
----------------------------------
- Float or double type
- Local to many functions and classes
- Value of output function
- Height


.. _zmax:

zmax
----------------------------------
- Float or double type
- Local to :ref:`w3d_compute_min_max` and :ref:`w3d_targa_output_surface`
- Maximum height of :ref:`z`


.. _zmin:

zmin
----------------------------------
- Float or double type
- Local to :ref:`w3d_compute_min_max` and :ref:`w3d_targa_output_surface`
- Minimum height of :ref:`z`




