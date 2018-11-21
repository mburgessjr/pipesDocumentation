Variables
=================================


.. _a:

a
---------------------------------
- NumPy array object
- Local to :ref:`Network` or :ref:`PyNetwork`
- Array of gravity wavespeeds in all pipes


.. _AA:

A
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Denotes the cross-sectional area of the pipe


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


.. _a0s:

a0s
---------------------------------
- Array type
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Vector with constant initial cross-sectional area values for each edge


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
- Local to :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, :ref:`Junction3 <Junction3>`, and :ref:`PyNetwork`
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


.. _Cl:

Cl
---------------------------------
- Float or double type
- Local to pipe
- Indicates chlorine concentration of pipe


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


.. _cmax:

cmax
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Maximum wave speed encountered


.. _conn:

conn
---------------------------------
- NumPy array object
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Array of integers of length double :ref:`Nedges <Nedges>`
- Where row i = [start node, end node] for pipe number i


.. _D:

D
---------------------------------
- Float or double type
- Local to pipe
- Pipe diameter in meters


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


.. _Eta:

Eta
---------------------------------
- Float or double type
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Hydrostatic pressure term
- Riemann invariant


.. _evol:

evol
---------------------------------
- Float or double type
- Local to :ref:`getTheGoddamnVolume <getTheGoddamnVolume>`
- Volume of the :ref:`Channel <Channel>`


.. _fc:

fc
---------------------------------
- The name of .config file to be loaded
- Local to multiple functions and classes such as :ref:`PyNetwork <PyNetwork>`
- The file is used with :ref:`fin <fin>` and :ref:`channeltype <channeltype>` to build the :ref:`PyNetwork <PyNetwork>` object
- It contains information about number of cells, time steps, etc.


.. _fconfig:

fconfig
---------------------------------
- The name of .config file to be loaded
- Local to multiple functions and classes such as :ref:`PyNetwork <PyNetwork>`
- The file is used with :ref:`fin <fin>` and :ref:`channeltype <channeltype>` to build the :ref:`PyNetwork <PyNetwork>` object
- It contains information about number of cells, time steps, etc.


.. _fi:

fi
---------------------------------
- The name of the .inp file to be loaded
- Local to multiple functions and classes such as :ref:`PyNetwork <PyNetwork>`
- The file is used with :ref:`fconfig` and :ref:`channeltype <channeltype>` to build the :ref:`PyNetwork <PyNetwork>` object
- It contains the network geometry including connectivity, lengths and elevations
- The file can be generated by EPANET (however this requires the use of cleanup.py to change the naming scheme)


.. _fin:

fin
---------------------------------
- The name of the .inp file to be loaded
- Local to multiple functions and classes such as :ref:`PyNetwork <PyNetwork>`
- The file is used with :ref:`fconfig` and :ref:`channeltype <channeltype>` to build the :ref:`PyNetwork <PyNetwork>` object
- It contains the network geometry including connectivity, lengths and elevations
- The file can be generated by EPANET (however this requires the use of cleanup.py to change the naming scheme)


.. _Fourier:

Fourier
---------------------------------
- Integer type
- Local to :ref:`getTimeSeries <getTimeSeries>`
- Binary vaue giving the model type that should be generated
- Either a Fourier series or Hermite spline


.. _H:

H
---------------------------------
- Float or double type
- Local to :ref:`Channel <Channel>`
- Pressure head


.. _i:

i
---------------------------------
- Integer type
- Local to multiple functions and classes, cheifly classes :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>`
- Pipe index of a network


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


.. _L:

L
---------------------------------
- Float or double type
- Local to pipe
- Pipe length in meters


.. _Ls:

Ls
---------------------------------
- Array type of length :ref:`Nedges <Nedges>`
- Local to :ref:`PyNetwork <PyNetwork>`
- Holds number of grid points for each edge


.. _M:

M
---------------------------------
- Integer type
- Local to :ref:`PyNetwork <PyNetwork>`
- Gives number of time steps


.. _Mi:

Mi
---------------------------------
- Integer type
- Local to :ref:`setupNetwork <setupNetwork>`
- Gives index of :ref:`M <M>`


.. _Mrs:

Mrs
---------------------------------
- Array type of length :ref:`Nedges <Nedges>`
- Local to :ref:`PyNetwork <PyNetwork>`
- Holds Manning roughness coefficients for each edge 


.. _N:

N
---------------------------------
- Integer type
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Number of cells


.. _Nedges:

Nedges
---------------------------------
- Integer type
- Local to :ref:`PyNetwork <PyNetwork>`
- Denotes the number of edges


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
- NumPy array object
- Local to :ref:`PyNetwork <PyNetwork>`
- Array of integers of length :ref:`Nedges <Nedges>`
- Element i is the number of cells in pipe i


.. _Nvar:

Nvar
---------------------------------
- Integer type
- Local to :ref:`PyNetwork <PyNetwork>`
- Denotes number of degrees of freedom per edges
- Currently supported models have 2 (cross sectional area :ref:`A <AA>` and discharge :ref:`Q <QQ>`)


.. _p:

p
---------------------------------
- Boolean type
- Local to various functions
- Gives statement on pressurization of pipe


.. _PE:

PE
---------------------------------
- Float or double type
- Local to :ref:`PyNetwork <PyNetwork>`
- Potential energy


.. _reflect:

reflect
---------------------------------
- Integer type
- Local to :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, or :ref:`Junction3 <Junction3>`
- Either -1, 0, or 1 in value
- Denotes the reflection cuased by the boundary


.. _S0s:

S0s
---------------------------------
- Array type of length :ref:`Nedges <Nedges>`
- Local to :ref:`Network <Network>` or :ref:`PyNetwork <PyNetwork>`
- Holds length of each edge 


.. _t:

t
---------------------------------
- Float or double type
- Global
- Time


.. _T:

T
---------------------------------
- Float or double type
- Local to :ref:`PyNetwork <PyNetwork>`
- Gives full simulated time period


.. _Ts:

Ts
---------------------------------
- Float or double type
- Local to pipe
- Preissman slot width of pipe


.. _valvetimes:

valvetimes
---------------------------------
- Dictionary object
- Local to :ref:`Junction2 <Junction2>` class
- Time series of valve timings
- Maps time to location


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


.. _q0s:

q0s
---------------------------------
- Array type
- Local to :ref:`PyNetwork <PyNetwork>`
- Vector with constant initial discharge values for each edge


.. _whichend:

whichend
---------------------------------
- Integer type
- Local to :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, or :ref:`Junction3 <Junction3>`
- Either 0 or 1 in value
- Described which boundary exists on
- 0 indicates :ref:`x <x>` = 0 (the left), 1 indicates :ref:`x <x>` = :ref:`L <L>` (the right)


.. _ws:

ws
---------------------------------
- Array type of length :ref:`Nedges <Nedges>`
- Local to :ref:`PyNetwork <PyNetwork>`
- Holds width/diameter of each edge 


.. _x:

x
---------------------------------
- Float or double type
- Global
- Space
