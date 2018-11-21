Functions
=================================


.. _boundaryFluxes:

boundaryFluxes(self, :ref:`dt <dt>`)
---------------------------------
- Method of classes :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, and :ref:`Junction3 <Junction3>`
- Defined explicitly in :ref:`network.cpp <network.cpp>`
- Separate definitions for each class, for :ref:`Junction1 <Junction1>` input of :ref:`dt <dt>` is not taken
- Applies boundary conditions to the end of a single pipe
- Computation is dependant on :ref:`reflect <reflect>`, :ref:`whichend <whichend>`, and :ref:`bvaltype <bvaltype>`
- Returns nothing


.. _Clhist:

Clhist(self, :ref:`i <i>`)
---------------------------------
- Attribute of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Requires pipe number :ref:`i <i>`
- Returns an array locally called Clhist
- This array holds a history of pressurization states :ref:`Cl <Cl>`
- Clhist = [Cl_0, Cl_1, ... Cl_n-1, Cl_n] at time step :ref:`n <n>`


.. _EulerStep:

EulerStep(self, :ref:`dt <dt>`)
---------------------------------
- Method of the :ref:`Network <Network>` class
- Defined in :ref:`network.cpp <network.cpp>`
- Takes input parameters self and :ref:`dt <dt>`
- Does the literal time stepping
- Calls :ref:`boundaryFluxes <boundaryFluxes>` for every increment of size in all junctions
- Returns nothing


.. _getAveGradH:

getAveGradH(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>` classes
- Defined explicitly in :ref:`network.cpp <network.cpp>` as a method of :ref:`Network <Network>` class
- Defined as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings <allthethings.pyx>`, calling the definition in :ref:`network.cpp <network.cpp>`
- Returns the average gradient at ith time step
- That gradient being the change in :ref:`H <H>` with respect to :ref:`x <x>`


.. _getKCl:

getKCl(self, :ref:`A <A>`, :ref:`Q <QQ>`)
---------------------------------
- Method of the :ref:`Channel <Channel>`
- Defined in :ref:`channel.cpp <channel.cpp>`
- Finds the Chlorine coefficient of a pipe based on specified inputs :ref:`A <A>` and :ref:`Q <QQ>`
- Returns :ref:`K <KK>`
- Also a method of the :ref:`PyNetwork <PyNetwork>` class in :ref:`allthethings.pys <allthethings.pyx>`
- But here the pipe index :ref:`i <i>` must be specified as well to grab the right object from :ref:`channels <channels>`


.. _getKE:

getKE(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>` classes
- Defined explicitly in :ref:`network.cpp <network.cpp>` as a method of :ref:`Network <Network>` class
- Defined as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings <allthethings.pyx>`, calling the definition in :ref:`network.cpp <network.cpp>`
- Takes self and :ref:`i <i>` inputs
- Gives kinetic energy of network
- Does so by summing :ref:`KE <KE>` of channels
- Returns :ref:`KE <KE>` as float or double


.. _getP:

getP(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined in :ref:`allthethings.pyx <allthethings.pyx>`
- References the :ref:`Channel <Channel>` object of pipe :ref:`i <i>`, returns :ref:`p <p>` statement on pressurization


.. _getKE:

getPE(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>` classes
- Defined explicitly in :ref:`network.cpp <network.cpp>` as a method of :ref:`Network <Network>` class
- Defined as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings <allthethings.pyx>`, calling the definition in :ref:`network.cpp <network.cpp>`
- Takes self and :ref:`i <i>` inputs
- Gives potential energy of network
- Does so by summing :ref:`PE <PE>` of channels
- Returns :ref:`PE <PE>` as float or double


.. _getTheGoddamnVolume:

getTheGoddamnVolume(self)
---------------------------------
- Defined as an implementation of the :ref:`Channel <Channel>` class
- Takes no input parameters outside the :ref:`Channel <Channel>` object itself
- Defined in :ref:`channel.cpp <channel.cpp>`
- Returns the volume of the channel
- Computes volume by multiplying sum of cell values of :ref:`A <A>` by :ref:`dx <dx>`


.. _getTimeSeries:

getTimeSeries(:ref:`bvals <bvals>`, :ref:`x <x>`, :ref:`m <m>`, :ref:`M <M>`, :ref:`T <T>`, :ref:`Fourier <Fourier>`)
---------------------------------
- Defined in :ref:`setupandrun.cpp <setupandrun.cpp>`
- Takes input parameters :ref:`bvals <bvals>`, :ref:`x <x>`, :ref:`m <m>`, :ref:`M <M>`, :ref:`T <T>`, and :ref:`Fourier <Fourier>`
- Generates either a discrete Fourier mode or Hermite spline based on the binary value of :ref:`Fourier`
- Returns nothing


.. _getTotalVolume:

getTotalVolume(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>` classes
- Defined explicitly in :ref:`network.cpp <network.cpp>` as a method of :ref:`Network <Network>` class
- Defined as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings <allthethings.pyx>`, calling the definition in :ref:`network.cpp <network.cpp>`
- Takes no input outside self
- Gives volume of network
- Calls :ref:`getTheGoddamnVolume <getTheGoddamnVolume>` for all channels
- Adds these calls and returns sum


.. _idx_t:

idx_t(self, i, j, :ref:`n <n>`, k)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined in :ref:`allthethings.pyx <allthethings.pyx>`
- Takes the index of ith variable (either 0 or 1) at :ref:`x <x>` location j at time step :ref:`n <n>` in pipe k
- Index variables local to this function are atypical, i does not represent the pipe index as it usually does, instead k is used for this
- References the integer :ref:`N <N>` of :ref:`channels <channels>` element k
- Uses these values to calculate integer return


.. _HofA:

HofA(:ref:`A <A>`, :ref:`D <D>`, :ref:`At <At>`, :ref:`Ts <Ts>`, :ref:`p <p>`)
---------------------------------
- Method of the :ref:`Channel <Channel>` class
- Defined explicitly in :ref:`channel.cpp <channel.cpp>`
- Takes inputs :ref:`A <A>`, :ref:`D <D>`, :ref:`At <At>`, :ref:`Ts <Ts>` and :ref:`p <p>`
- Yet, these parameters can be found as pre-existing attributes of the :ref:`Channel <Channel>` class
- Finds height of fluid based on current cross-sectional area amongst other factors
- Returns the height in meters as a double or float type
- Can also be called from the :ref:`PyNetwork <PyNetwork>` class
- In that case, the implementation of the :ref:`Channel <Channel>` class is called for all :ref:`i <i>`, returning an array of heights


.. _phist:

phist(self, :ref:`i <i>`)
---------------------------------
- Attribute of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Requires pipe number :ref:`i <i>`
- Returns an array locally called phist
- This array holds a history of pressurization states :ref:`p <p>`
- phist = [p_0, p_1, ... p_n-1, p_n] at time step :ref:`n <n>`


.. _pressureSpaceSeries:

pressureSpaceSeries(self, :ref:`i <i>`, :ref:`k <k>`)
---------------------------------
- Attribute of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Returns an array of pressure head as a function of SPACE at cell :ref:`k <k>` in pipe :ref:`i <i>`
- References :ref:`Channel <Channel>` object of pipe :ref:`i <i>` to do so


.. _pressureTimeSeries:

pressureTimeSeries(self, :ref:`i <i>`, :ref:`k <k>`)
---------------------------------
- Attribute of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Returns an array of pressure head as a function of TIME at cell :ref:`k <k>` in pipe :ref:`i <i>`
- References :ref:`Channel <Channel>` object of pipe :ref:`i <i>` to do so


.. _qfunction:

q(self, :ref:`i <i>`)
---------------------------------
- Defined within the :ref:`PyNetwork <PyNetwork>` class
- Defined in :ref:`allthethings.pyx <allthethings.pyx>`
- Takes pipe number :ref:`i <i>`
- Returns a NumPy array object with current values of dynamical variables in given pipe
- The ith element of list q is an NumPy array pointing at the data in pipe i
- Easy way to call: q = [n1.q(i) for i in range(n1.Nedges)]


.. _qhist:

qhist(self, :ref:`i <i>`)
---------------------------------
- Attribute of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Requires pipe number :ref:`i <i>`
- Returns an array locally called qhist
- This array holds a history of states :ref:`q <q>` = (:ref:`A <A>`, :ref:`Q <QQ>`)
- q_n = [A_left, A_0, ... A_n-1, A_right, Q_left, Q_0, ... Q_n-1, Q_right] at time step :ref:`n <n>`


.. _reset:

reset(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined in :ref:`allthethings.pyx <allthethings.pyx>`
- Resets time steps to x=zero for all elements in :ref:`channels <channels>`
- Therefore, reseting the network to zero time
- No inputs or returns


.. _runForwardProblem:

runForwardProblem(self, :ref:`dt <dt>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>` classes
- Defined explicitly in :ref:`network.cpp <network.cpp>` as a method of the :ref:`Network <Network>` class
- Defined as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings <allthethings.pyx>`, calling the definition in :ref:`network.cpp <network.cpp>`
- Takes input parameters self and :ref:`dt <dt>`
- Makes :ref:`M <M>` time time steps, each of length :ref:`dt <dt>` by incrementing :ref:`nn <nn>` and calling :ref:`stepRK3_SSP`
- Returns nothing


.. _setbVal:

setbVal(self, :ref:`bvalnew <bvalnew>`)
---------------------------------
- Method of classes :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, :ref:`Junction3 <Junction3>`, and :ref:`PyNetwork <PyNetwork>`
- Literally takes input of :ref:`bvalnew <bvalnew>` and adds it to :ref:`bvals <bvals>` array
- No return


.. _setC10:

setCl0(self, :ref:`x <x>`)
---------------------------------
- Method of the :ref:`Channel <Channel>` class
- Defined in :ref:`channel.cpp <channel.cpp>`
- Sets initial Chlorine levels in specified pipe
- Also a method of the :ref:`PyNetwork <PyNetwork>` class in :ref:`allthethings.pys <allthethings.pyx>`
- But here the pipe index :ref:`i <i>` must be specified as well to grab the right object from :ref:`channels <channels>`


.. _setClkw:

setClkw(self, :ref:`K <K>`)
---------------------------------
- Method of the :ref:`Channel <Channel>` class
- Defined in :ref:`channel.cpp <channel.cpp>`
- Sets Chlorine wall coefficient for specified pipe
- Also a method of the :ref:`PyNetwork <PyNetwork>` class in :ref:`allthethings.pys <allthethings.pyx>`
- But here the pipe index :ref:`i <i>` must be specified as well to grab the right object from :ref:`channels <channels>`


.. _setIC:

setIC(self, :ref:`i <i>`, :ref:`a0s <a0s>`, :ref:`q0 <q0s>`):
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Sets initial conditions in pipe i
- Takes NumPy array objects :ref:`a0s <a0s>` and :ref:`q0s <q0s>` of length :ref:`N <N>`
- Returns nothing


.. _setValveTimes:

setValveTimes(self, :ref:`x <x>`)
---------------------------------
- Method of the :ref:`Junction2 <Junction2>`
- Defined explicitly in :ref:`channel.cpp <channel.cpp>`
- Takes an :ref:`x <x>` value for a specific junction object and adds the location to :ref:`valvetimes <valvetimes>`
- This is a dictionary that maps time to valve timing
- Referenced as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings.pyx <allthethings.pyx>` that does the same thing, except requires pipe index :ref:`i <i>` as well


.. _setupNetwork:

setupNetwork(:ref:`fin <fin>`, :ref:`fconfig <fconfig>`, :ref:`M <M>`, :ref:`Mi <Mi>`, :ref:`T <T>`, :ref:`channeltype <channeltype>`)
---------------------------------
- Defined in :ref:`setupandrun.cpp <setupandrun.cpp>`
- Takes input parameters :ref:`fin <fin>`, :ref:`fconfig <fconfig>`, :ref:`M <M>`, :ref:`Mi <Mi>`, :ref:`T <T>`, and :ref:`channeltype <channeltype>`
- First opens the input and configuration files
- Processes information about the network layout and components
- Returns Network object
- Used to initialize the :ref:`PyNetwork <PyNetwork>` class


.. _showCurrentData:

showCurrentData(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Simply prints out a table of data represneting states at current time (:ref:`nn <nn>` * :ref:`T <T>`) / :ref:`M <M>`
- No input or return


.. _showExternalBoundaries:

showExternalBoundaries(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Gives information on junctions and boundary conditions by printing
- No input or return


.. _showLayout:

showLayout(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Simply prints out a table of pipes and what nodes they're connected to
- No input or return


.. _stepRK3_SSP:

stepRK3_SSP(self, :ref:`dt <dt>`)
---------------------------------
- Method of the :ref:`Network <Network>` class
- Defined in :ref:`network.cpp <network.cpp>`
- Takes input parameters self and :ref:`dt <dt>`
- Increments :ref:`channels <channels>` and calls :ref:`EulerStep <EulerStep>`
- Two indexes of i (for channels) and j (for :ref:`Nedges <Nedges>`)
- Returns nothing












