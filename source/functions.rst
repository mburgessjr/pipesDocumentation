Functions
=================================


.. _AofH:

AofH(self, :ref:`h`, :ref:`p`)
---------------------------------
- Basely a method of the :ref:`PyPipe_ps`, :ref:`Channel`, and :ref:`Cuniform` and :ref:`Cpreiss` classes
- Defined in :ref:`channel.cpp` as an implementation of :ref:`Cpreiss`
- However defined as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Takes input of :ref:`h` and boolean :ref:`p`
- Literally gives area in terms of height


.. _AofPhi:

AofPhi(self, :ref:`Phi`, :ref:`D`, :ref:`At`, :ref:`Ts`, :ref:`P`)
---------------------------------
- Method of the :ref:`PyPipe_ps` and :ref:`Channel <Channel>` classes
- Defined independently and explicitly in :ref:`channel.cpp <channel.cpp>`
- However defined exclusively and more simply as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Takes inputs of :ref:`Phi`, :ref:`D`, :ref:`At`, :ref:`Ts`, and :ref:`P`
- Gives :ref:`A <AA>` from :ref:`Phi`
- Returns :ref:`A <AA>` of course


.. _boundaryFluxes:

boundaryFluxes(self, :ref:`dt <dt>`)
---------------------------------
- Method of classes :ref:`Junction1 <Junction1>`, :ref:`Junction2 <Junction2>`, and :ref:`Junction3 <Junction3>`
- Defined explicitly in :ref:`network.cpp <network.cpp>`
- Separate definitions for each class, for :ref:`Junction1 <Junction1>` input of :ref:`dt <dt>` is not taken
- Applies boundary conditions to the end of a single pipe
- Computation is dependant on :ref:`reflect <reflect>`, :ref:`whichend <whichend>`, and :ref:`bvaltype <bvaltype>`
- Returns nothing


.. _Cgravfunction:

Cgrav(self, :ref:`A <AA>`, :ref:`D`, :ref:`At`, :ref:`Ts`, :ref:`P`)
---------------------------------
- Method of the :ref:`PyPipe_ps`, :ref:`Channel`, :ref:`Cuniform`, and :ref:`Cpreiss` classes
- Independently defined in :ref:`channel.cpp`
- However defined as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Takes input parameters :ref:`A <AA>`, :ref:`D`, :ref:`At`, :ref:`Ts`, and boolean :ref:`P`
- Returns gravity wavespeed :ref:`cgrav`
- Uses an equation of the form sqrt(:ref:`g`*:ref:`A <AA>`/:ref:`l`) to do so


.. _Channelfunction:

Channel(:ref:`Nin`, :ref:`win`, :ref:`Lin`, :ref:`Min`, :ref:`a`, :ref:`kwin`)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Constructs :ref:`Channel` object
- Object holds dynamic :ref:`q` and updates
- Attributed values cleard by destructing :ref:`~Channel <Channeldestructor>`


.. _Channeldestructor:

~Channel(self)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Destructs :ref:`Channel` object by deleting all associated arrays
- Opposite to :ref:`Channel <Channelfunction>`


.. _ChebEval:

ChebEval(alpha, n, x)
---------------------------------
- Independent function
- Defined in :ref:`chebyshevlite.h`
- Uses 2-term recursion to evaluate Chebyshev polynomial
- Defined over x points in [-1, 1]
- Returns float value


.. _check_reduction:

check_reduction(self)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in the :ref:`levmar.cpp`
- Checks reduction of curent algorithmic estimate
- Updates :ref:`x` and delta for :ref:`Levmar`
- Returns integer of this updated :ref:`delta` value


.. _check_reduction_roundoff_regime:

check_reduction_roundoff_regime(self, :ref:`rho`)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Updates :ref:`delta` via :ref:`update_delta <update_delta>` based on regime
- Returns integer of this updated value


.. _chkder:

chkder(self, :ref:`dx`)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Increments object by :ref:`dx`
- Uses :ref:`x` as a basepoint


.. _Clhist:

Clhist(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Requires pipe number :ref:`i <i>`
- Returns an array locally called Clhist
- This array holds a history of pressurization states :ref:`Cl <Cl>`
- Clhist = [Cl_0, Cl_1, ... Cl_n-1, Cl_n] at time step :ref:`n <n>`


.. _compute_diag:

compute_diag(self, nD)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Computes diagonal values of :ref:`D` for each increment of integer nD


.. _compute_f:

compute_f(self)
---------------------------------
- Method of the :ref:`Levmar`, :ref:`PyMystery_BC`, and :ref:`PyBC_opt_dh` classes
- Defined explicitly in :ref:`levmar.cpp`, and as an implementation of :ref:`PyMystery_BC` and :ref:`PyBC_opt_dh` in :ref:`allthethings.pyx`
- Computes :ref:`f` for :ref:`Levmar`


.. _compute_g:

compute_g(self)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Computes :ref:`g` for :ref:`Levmar`


.. _compute_J:

compute_J(self)
---------------------------------
- Method of the :ref:`Levmar`, :ref:`bc_opt_dh_c`, and :ref:`nlEig` classes
- Defined in :ref:`levmar.cpp`, and as an implementation of :ref:`bc_opt_dh_c` in :ref:`optdetritus.h`
- Computes Jacobian for :ref:`Levmar`
- Required in multivariable parameterized computations


.. _compute_p2:

compute_p2(self)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Computes :ref:`p2` for the object


.. _compute_r:

compute_r(self)
---------------------------------
- Method of the :ref:`Levmar`, :ref:`bc_opt_dh_c`, and :ref:`nlEig` classes
- Defined in :ref:`levmar.cpp`, and as an implementation of :ref:`bc_opt_dh_c` in :ref:`optdetritus.h`
- Computes :ref:`r` for :ref:`Levmar`
- Uses :ref:`x` as an input for computation


.. _dump:

dump(self)
---------------------------------
- Method of the :ref:`PyMystery_BC`, :ref:`PyBC_opt_dh`, and :ref:`Levmar` classes
- Defined in :ref:`levmar.cpp` and as an implementation of :ref:`PyMystery_BC` and :ref:`PyBC_opt_dh` in :ref:`allthethings.pyx`
- Prints some information and writes to a file
- Doesn't change any values, simple print function


.. _Etafunction:

Eta(self, :ref:`A <AA>`, :ref:`D`, :ref:`At`, :ref:`Ts`, :ref:`P`)
---------------------------------
- Method of classes :ref:`PyPipe_ps` and :ref:`Channel`
- Independently defined in :ref:`channel.cpp`
- However defined exclusively and more simply as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Takes inputs and calculates :ref:`Eta`
- Returns :ref:`Eta`


.. _EulerStep:

EulerStep(self, :ref:`dt <dt>`)
---------------------------------
- Method of the :ref:`Network <Network>` class
- Defined in :ref:`network.cpp <network.cpp>`
- Takes input parameter :ref:`dt <dt>`
- Does the literal time stepping
- Calls :ref:`boundaryFluxes <boundaryFluxes>` for every increment of size in all junctions
- Returns nothing
- Similar but not nearly equivalent to :ref:`stepEuler <stepEuler>`


.. _fakeAofh:

fakeAofh(self, :ref:`h`, :ref:`p`)
---------------------------------
- Basely a method of the :ref:`Channel`, :ref:`Cuniform`, and :ref:`Cpreiss` classes
- Defined in :ref:`channel.cpp` as an implementation of :ref:`Cpreiss`
- However defined exclusively and more simply as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Gives area in terms of height for the "negative Preissman model"
- Essentially :ref:`AofH <AofH>` for this negative model


.. _fakehofA:

fakehofA(self, :ref:`A <AA>`, :ref:`p`)
---------------------------------
- Basely a method of the :ref:`Channel`, :ref:`Cuniform`, and :ref:`Cpreiss` classes
- Defined in :ref:`channel.cpp` as an implementation of :ref:`Cpreiss`
- However defined exclusively and more simply as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Gives height in terms of area for the "negative Preissman model"
- Essentially :ref:`HofA <HofA>` for this negative model


.. _findOmega:

findOmega(:ref:`Astar`, Ak, :ref:`Ps`, Pk)
---------------------------------
- Method of the :ref:`Cpreiss` class
- Defined in :ref:`channel.cpp`
- Computes :ref:`Omega` to be used by the :ref:`speedsHLL <speedsHLL>` estimate
- Takes inputs :ref:`Astar`, Ak, :ref:`Ps`, and Pk
- Where Ak is either :ref:`q1m` or :ref:`q1p` and Pk is the corresponding :ref:`Pm` or :ref:`ppp`


.. _getAveGradH:

getAveGradH(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>`, :ref:`Network <Network>`, :ref:`PyPipe_ps`, and :ref:`Channel` classes
- Defined explicitly in :ref:`network.cpp <network.cpp>` as a method of :ref:`Network <Network>` class
- Defined as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings <allthethings.pyx>`, calling the definition in :ref:`network.cpp <network.cpp>`
- Returns the average gradient at ith time step
- That gradient being the change in :ref:`H <H>` with respect to :ref:`x <x>`


.. _getBCtimeseries:

getBCtimeseries(self, :ref:`i`)
---------------------------------
- Method of the :ref:`PyMystery_BC` and :ref:`PyBC_opt_dh` classes
- Defined in :ref:`allthethings.pyx`
- Implements the function :ref:`getTimeSeries` as a method of given object
- Returns :ref:`bvals`


.. _getBCTimeSeries2:

getBCTimeSeries2(self)
---------------------------------
- Method of the :ref:`PyBC_opt_dh` class
- Defined in :ref:`allthethings.pyx`
- Implements the function :ref:`setTimeSeries` as a method of :ref:`PyBC_opt_dh`
- Returns :ref:`bvals`


.. _getChebNodes:

getChebNodes(xx, n)
---------------------------------
- Independent function
- Defined in :ref:`chebyshevlite.h`
- Takes array xx of length n
- Fills array with n standard Chebyshev nodes on the closed interval [-1, 1]
- No return but array is updated


.. _getFlowThrough:

getFlowThrough(self, :ref:`dt`)
---------------------------------
- Method of the :ref:`Junction1` class
- Defined in :ref:`channel.cpp`
- Takes sole input of :ref:`dt`
- Computes total flow from left to right as a function of discharge over past time
- Returns this flow through the pipe


.. _getHydRad:

getHydRad(self, :ref:`A <AA>`)
---------------------------------
- Basely a method of the :ref:`Channel`, :ref:`Cuniform`, and :ref:`Cpreiss` classes
- Defined as an implementation of :ref:`Cpreiss` in :ref:`channel.cpp`
- However defined exclusively and more simply as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Taks sole input :ref:`A <AA>` and returns hydraulic radius :ref:`R <RR>`
- This value is given by the cross-sectional area divided by the wetted perimeter


.. _getKCl:

getKCl(self, :ref:`ai`, :ref:`qi`)
---------------------------------
- Method of the :ref:`Channel <Channel>` class
- Defined in :ref:`channel.cpp <channel.cpp>`
- Finds the Chlorine coefficient of a pipe based on specified inputs :ref:`ai` and :ref:`qi`
- Returns :ref:`K <KK>`
- Also a method of the :ref:`PyNetwork <PyNetwork>` class in :ref:`allthethings.pys <allthethings.pyx>`
- But here the pipe index :ref:`i <i>` must be specified as well to grab the right object from :ref:`channels <channels>`


.. _getKE:

getKE(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>`, :ref:`Network <Network>`, and :ref:`Channel` classes
- Defined explicitly in :ref:`network.cpp <network.cpp>` as a method of :ref:`Network <Network>` class
- Defined as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings <allthethings.pyx>`, calling the definition in :ref:`network.cpp <network.cpp>`
- Takes self and :ref:`i <i>` inputs
- Gives kinetic energy of network
- Does so by summing :ref:`KE <KE>` of channels
- Returns :ref:`KE <KE>` as float or double


.. _getMassTransCoeff:

getMassTransCoeff(self, :ref:`ui`)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Finds mass transfer coefficient :ref:`kf` based on input :ref:`ui`
- From Rossman 1994 J. Env. Eng page 805


.. _getP:

getP(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined in :ref:`allthethings.pyx <allthethings.pyx>`
- References the :ref:`Channel <Channel>` object of pipe :ref:`i <i>`, returns :ref:`p <p>` statement on pressurization


.. _getPE:

getPE(self, :ref:`i <i>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>`, :ref:`Network <Network>`, and :ref:`Channel` classes
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
- Computes volume by summin cell values retrieved by multiplying :ref:`A <AA>` by :ref:`dx <dx>`


.. _getTimeSeries:

getTimeSeries(:ref:`bvals <bvals>`, :ref:`x <x>`, :ref:`m <m>`, :ref:`M <MM>`, :ref:`T <TTT>`, :ref:`Fourier <Fourier>`)
---------------------------------
- Defined in :ref:`setupandrun.cpp <setupandrun.cpp>` and equivalently in :ref:`basic_time_series.h`
- Takes input parameters :ref:`bvals <bvals>`, :ref:`x <x>`, :ref:`m <m>`, :ref:`M <MM>`, :ref:`T <TTT>`, and :ref:`Fourier <Fourier>`
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


.. _HofA:

HofA(self, :ref:`A <AA>`, :ref:`D <D>`, :ref:`At <At>`, :ref:`Ts <Ts>`, :ref:`p <p>`)
---------------------------------
- Method of the :ref:`PyPipe_ps` and :ref:`Channel <Channel>` classes
- Defined independently and explicitly in :ref:`channel.cpp <channel.cpp>`
- However defined exclusively and more simply as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Takes inputs :ref:`A <AA>`, :ref:`D <D>`, :ref:`At <At>`, :ref:`Ts <Ts>` and :ref:`p <p>`
- Yet, these parameters can be found as pre-existing attributes of the :ref:`Channel <Channel>` class
- Finds height of fluid based on current cross-sectional area amongst other factors
- Literally returns :ref:`H` in terms of :ref:`A <AA>`
- Returns the height in meters as a double or float type
- Can also be called from the :ref:`PyNetwork <PyNetwork>` class
- In that case, the implementation of the :ref:`Channel <Channel>` class is called for all :ref:`i <i>`, returning an array of heights


.. _idx:

idx(self, :ref:`i_in`, :ref:`j_in`)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.h`
- Simple indexing function to access :ref:`q`
- Returns integer


.. _idx_t:

idx_t(self, i, j, :ref:`n <n>`, k)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined in :ref:`allthethings.pyx <allthethings.pyx>`
- Takes the index of ith variable (either 0 or 1) at :ref:`x <x>` location j at time step :ref:`n <n>` in pipe k
- Index variables local to this function are atypical, i does not represent the pipe index as it usually does, instead k is used for this
- References the integer :ref:`N <NNN>` of :ref:`channels <channels>` element k
- Uses these values to calculate integer return


.. _Junction1function:

Junction1(:ref:`Channel`, :ref:`whichend`, :ref:`bval`, :ref:`bvaltype`)
---------------------------------
- Method of the :ref:`Junction1` class
- Defined in :ref:`channel.cpp`
- Constructs the :ref:`Junction1` object
- Requires a tied :ref:`Channel` object as an input 


.. _Junction1destructor:

~Junction1()
---------------------------------
- Method of the :ref:`Junction1` class
- Defined in :ref:`channel.cpp`
- Destructs the :ref:`Junction1` object
- More specifically, clears :ref:`bvals` and :ref:`Clbval`


.. _Junction2function:

Junction2(:ref:`Channel` 0, :ref:`Channel` 1, :ref:`whichend0`, :ref:`whichend1`, :ref:`valveopen`)
---------------------------------
- Method of the :ref:`Junction2` class
- Defined in :ref:`channel.cpp`
- Constructs the :ref:`Junction2` object
- Requires two tied :ref:`Channel` objects to build


.. _Junction3function:

Junction3(:ref:`Channel` 0, :ref:`Channel` 1, :ref:`Channel` 2, :ref:`whichend0`, :ref:`whichend1`, :ref:`whichend2`)
---------------------------------
- Method of the :ref:`Junction3` class
- Defined in :ref:`channel.cpp`
- Constructs the :ref:`Junction3` object
- Requires two tied :ref:`Channel` objects to build


.. _levmarfunction:

levmar(:ref:`m`, :ref:`n`)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Constructs a :ref:`Levmar` object
- With input dimensions of :ref:`m` x :ref:`n`
- Meant to minimize :ref:`f`


.. _max3:

max3(a, b, c)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Takes three float or double types (a, b, c)
- Simply returns the maximum out of three inputs
- Needed for speed estimates


.. _min3:

min3(a, b, c)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Takes three float or double types (a, b, c)
- Simply returns the minimum out of three inputs
- Needed for speed estimates


.. _Newton:

Newton(:ref:`f`, :ref:`df`, :ref:`x0`, :ref:`tol`, :ref:maxitier`)
---------------------------------
- Equivalently defined in both :ref:`newton.h` and :ref:`newton.cpp`
- Takes inputs :ref:`f`, :ref:`df`, :ref:`x0`, :ref:`tol`, and :ref:`maxiter`
- Increments :ref:`x` from :ref:`x0` by subtracting :ref:`f` value divided by :ref:`df` until :ref:`maxiter` reached
- Returns final :ref:`x` value


.. _numFluxHLL:

numFluxHLL(:ref:`q1m`, :ref:`q1p`, :ref:`q2m`, :ref:`q2p`, :ref:`flux`, :ref:`Pm`, :ref:`ppp`)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Takes inputs :ref:`q1m`, :ref:`q1p`, :ref:`q2m`, :ref:`q2p`, :ref:`flux`, :ref:`Pm`, and :ref:`ppp`
- These are sort of datapoints for the state of the pipe on the both the left and right
- Updates Harten-Lax-van Leer (HLL) numerical flux
- Returns nothing
- Needed to do HLL speed estimates by :ref:`speedsHLL <speedsHLL>`


.. _pbarfunction:

pbar(self, :ref:`A <AA>`, :ref:`p`)
---------------------------------
- Method of the :ref:`PyPipe_ps`, :ref:`Channel`, :ref:`Cuniform`, and :ref:`Cpreiss` classes
- Defined in :ref:`channel.h` seperately as both implementations of :ref:`Cuniform` and :ref:`Cpreiss`
- Returns :ref:`pbar`


.. _PhiofA:

PhiofA(self, :ref:`A <AA>`, :ref:`D`, :ref:`At`, :ref:`Ts`, :ref:`P`)
---------------------------------
- Method of the :ref:`PyPipe_ps` and :ref:`Channel <Channel>` classes
- Defined independently and explicitly in :ref:`channel.cpp <channel.cpp>`
- However defined exclusively and more simply as an implementation of :ref:`Cuniform` in :ref:`channel.h`
- Takes inputs of :ref:`A <AA>`, :ref:`D`, :ref:`At`, :ref:`Ts`, and :ref:`P`
- Gives :ref:`Phi` from :ref:`A <AA>`
- Returns :ref:`Phi` of course


.. _phist:

phist(self, :ref:`i <i>`)
---------------------------------
- Attribute of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Requires pipe number :ref:`i <i>`
- Returns an array locally called phist
- This array holds a history of pressurization states :ref:`p <p>`
- phist = [p_0, p_1, ... p_n-1, p_n] at time step :ref:`n <n>`


.. _physFlux:

physFlux(:ref:`q1`, :ref:`q2`, :ref:`flux`, :ref:`P`)
---------------------------------
- Method of :ref:`Channel` objects
- Defined in :ref:`channel.cpp`
- Utilizes the de St. Venant flux function to designate flux array values
- Requires the :ref:`Eta <Etafunction>` function
- Has no return, but takes inputs :ref:`q1`, :ref:`q2`, :ref:`flux`, and :ref:`P`
- Where :ref:`q1` is equal to the first element of given :ref:`q`, and :ref:`q2` is the second


.. _pj:

pj(self, i)
---------------------------------
- Method of :ref:`Channel` objects
- Defined in :ref:`channel.h`
- Indexing function to access elements of :ref:`P` correctly
- Here, i is a simple indexed integer input, not the typical pipe index :ref:`i`
- Returns an integer one greater than the input i


.. _pj_t:

pj_t(self, i, :ref:`n`)
---------------------------------
- Method of :ref:`Channel` objects
- Defined in :ref:`channel.h`
- Indexing function to access  history of pressurization states
- Here, i is a simple indexed integer input, not the typical pipe index :ref:`i`
- Returns an integer


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
- Returns an array object with current values of dynamical variables in given pipe
- The ith element of list q is an array pointing at the data in pipe i
- Easy way to call: q = [n1.q(i) for i in range(n1.Nedges)]


.. _qhist:

qhist(self, :ref:`i <i>`)
---------------------------------
- Attribute of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Requires pipe number :ref:`i <i>`
- Returns an array locally called qhist
- This array holds a history of states :ref:`q <q>` = (:ref:`A <AA>`, :ref:`Q <QQ>`)
- q_n = [A_left, A_0, ... A_n-1, A_right, Q_left, Q_0, ... Q_n-1, Q_right] at time step :ref:`n <n>`


.. _quickWrite:

quickWrite(self, :ref:`where`, :ref:`which`, K, :ref:`T <TTT>`, :ref:`skip`)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Quickly writes out some run time information
- Takes inputs :ref:`where`, :ref:`which`, K, :ref:`T <TTT>`, and increment :ref:`skip`
- Here, K is equal to the length of :ref:`where` and :ref:`which`
- Returns nothing


.. _reset:

reset(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined in :ref:`allthethings.pyx <allthethings.pyx>`
- Resets time steps to x = zero for all elements in :ref:`channels <channels>`
- Therefore, reseting the network to zero time
- No inputs or returns


.. _runForwardProblem:

runForwardProblem(self, :ref:`dt <dt>`)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` and :ref:`Network <Network>` classes
- Defined explicitly in :ref:`network.cpp <network.cpp>` as a method of the :ref:`Network <Network>` class
- Defined as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings <allthethings.pyx>`, calling the definition in :ref:`network.cpp <network.cpp>`
- Takes input parameters self and :ref:`dt <dt>`
- Makes :ref:`M <MM>` time time steps, each of length :ref:`dt <dt>` by incrementing :ref:`nn <nn>` and calling :ref:`stepRK3_SSP`
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


.. _setClbVal:

setClbVal(self, ClbValnew)
---------------------------------
- Method of the :ref:`Junction1` and :ref:`PyPipe_ps` classes
- Defined in :ref:`channel.cpp`
- Updates :ref:`ClbVal` to input ClbValnew
- Input can be a single value or a nonconstant array
- If the input is a list, then each value in it will be mapped at the same index to :ref:`ClbVal`
- Else, all values of :ref:`ClbVal` become the constant value provided
- Returns nothing


.. _setClkw:

setClkw(self, :ref:`K <KK>`)
---------------------------------
- Method of the :ref:`Channel <Channel>` class
- Defined in :ref:`channel.cpp <channel.cpp>`
- Sets Chlorine wall coefficient for specified pipe
- Also a method of the :ref:`PyNetwork <PyNetwork>` class in :ref:`allthethings.pys <allthethings.pyx>`
- But here the pipe index :ref:`i <i>` must be specified as well to grab the right object from :ref:`channels <channels>`


.. _set_dist_mat_ptrs:

set_dist_mat_ptrs(a, b, c, d, e, f)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Sets pointers for 6 input matrices
- These matrices are likely attributes of the :ref:`Levmar` object
- Returns nothing


.. _set_gammaD:

set_gammaD(self, gD)
---------------------------------
- Method of :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Sets :ref:`gammaD` equal to input float gD


.. _setIC:

setIC(self, :ref:`i <i>`, :ref:`a0s <a0s>`, :ref:`q0 <q0s>`):
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Sets initial conditions in pipe i
- Takes NumPy array objects :ref:`a0s <a0s>` and :ref:`q0s <q0s>` of length :ref:`N <N>`
- Returns nothing


.. _set_init_params:

set_init_params(self)
---------------------------------
- Method of :ref:`Levmar`
- Defined explicitly in :ref:`levmar.cpp`
- Sets initial parameters of the :ref:`Levmar` class
- For example, this function defines :ref:`f` and :ref:`df` as 0


.. _setValveTimes:

setValveTimes(self, :ref:`x <x>`)
---------------------------------
- Method of the :ref:`Junction2 <Junction2>`
- Defined explicitly in :ref:`channel.cpp <channel.cpp>`
- Takes an :ref:`x <x>` value for a specific junction object and adds the location to :ref:`valvetimes <valvetimes>`
- This is a dictionary that maps time to valve timing
- Referenced as a method of :ref:`PyNetwork <PyNetwork>` in :ref:`allthethings.pyx <allthethings.pyx>` that does the same thing, except requires pipe index :ref:`i <i>` as well


.. _setupNetwork:

setupNetwork(:ref:`fin <fin>`, :ref:`fconfig <fconfig>`, :ref:`M <MM>`, :ref:`Mi <Mi>`, :ref:`T <T>`, :ref:`channeltype <channeltype>`)
---------------------------------
- Defined in :ref:`setupandrun.cpp <setupandrun.cpp>`
- Takes input parameters :ref:`fin <fin>`, :ref:`fconfig <fconfig>`, :ref:`M <MM>`, :ref:`Mi <Mi>`, :ref:`T <T>`, and :ref:`channeltype <channeltype>`
- First opens the input and configuration files
- Processes information about the network layout and components
- Returns Network object
- Used to initialize the :ref:`PyNetwork <PyNetwork>` class


.. _setq:

setq(self, :ref:`a0`, :ref:`q0`)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Initializes :ref:`q0` with NONCONSTANT data (:ref:`a0`, :ref:`q0`)
- In this case, inputs :ref:`a0` and :ref:`q0` are array types, which is atypical
- Returns nothing


.. _setq0:

setq0(self, :ref:`a0`, :ref:`q0`)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Initializes :ref:`q0` with CONSTANT data (:ref:`a0`, :ref:`q0`)
- In this case, inputs :ref:`a0` and :ref:`q0` are float or double types, as expected
- Returns nothing


.. _set_x:

set_x(self, xin)
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Assigns :ref:`x` to xin


.. _showCurrentData:

showCurrentData(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Simply prints out a table of data represneting states at current time (:ref:`nn <nn>` * :ref:`T <TTT>`) / :ref:`M <MM>`
- No input or return


.. _showExternalBoundaries:

showExternalBoundaries(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Gives information on junctions and boundary conditions by printing
- No input or return


.. _showGeom:

showGeom(self)
---------------------------------
- Method of the :ref:`PyPipe_ps`, :ref:`Channel`, :ref:`Cpreiss`, and :ref:`Cuniform` classes
- Defined in :ref:`channel.cpp`
- Prints information about the geometry of the pipe, such as if it has a slot or not, area, gridpoints, width, etc.


.. _showLayout:

showLayout(self)
---------------------------------
- Method of the :ref:`PyNetwork <PyNetwork>` class
- Defined explicitly in :ref:`allthethings.pyx <allthethings.pyx>`
- Simply prints out a table of pipes and what nodes they're connected to
- No input or return


.. _showp:

showp(self)
---------------------------------
- Method of :ref:`Channel`, :ref:`Cpreiss`, and :ref:`Cuniform` classes
- Defined in :ref:`channel.cpp`
- Prints pressure head of all cells in :ref:`channel`
- No inputs no outputs


.. _showVals:

showVals(self, Iwantq)
---------------------------------
- Method of :ref:`Channel`
- Defined in :ref:`channel.cpp`
- Simple print function that displays either all cell valus of :ref:`q` or :ref:`q0` based on the value of :ref:`Iwantq`


.. _solve:

solve(self, skipJ)
---------------------------------
- Method of the :ref:`Levmar`, :ref:`PyBC_opt_dh`, and :ref:`PyMystery_BC` classes
- Defined in :ref:`levmar.cpp` and as an implementation of :ref:`PyBC_opt_dh` and :ref:`PyMystery_BC` in :ref:`allthethings.pyx`
- Computes :ref:`f` and reports :ref:`r`
- Takes integer input skipJ, this indicates which Jacobian computations to ignore
- Only needs skipJ if there are Jacobians to skip
- Returns nothing


.. _speedsHLL:

speedsHLL(self, :ref:`q1m`, :ref:`q1p`, :ref:`q2m`, :ref:`q2p`, :ref:`s <s>`, :ref:`Pm`, :ref:`ppp`)
---------------------------------
- Method of :ref:`Channel`, :ref:`Cpreiss`, and :ref:`Cuniform` classes
- Defined as an implementation as both above classes individually in :ref:`channel.cpp`
- Takes above noted inputs self, :ref:`q1m`, :ref:`q1p`, :ref:`q2m`, :ref:`q2p`, :ref:`s <s>`, :ref:`Pm`, and :ref:`ppp`
- Used to estimate Harten-Lax-van Leer wave speeds based on Leon 2009
- Alternate to :ref:`speedsRoe <speedsRoe>`
- Doesn't return anything, simply updates variables local to object acted on


.. _speedsRoe:

speedsRoe(self, :ref:`q1m`, :ref:`q1p`, :ref:`q2m`, :ref:`q2p`, :ref:`s <s>`, :ref:`Pm`, :ref:`ppp`)
---------------------------------
- Method of :ref:`Channel`, :ref:`Cpreiss`, and :ref:`Cuniform` classes
- Defined in :ref:`channel.cpp`
- Takes above noted inputs self, :ref:`q1m`, :ref:`q1p`, :ref:`q2m`, :ref:`q2p`, :ref:`s <s>`, :ref:`Pm`, and :ref:`ppp`
- Gives Roe wave speed estimates
- Alternate to :ref:`speedsHLL <speedsHLL>`
- Doesn't return anything, simply updates variables local to object acted on


.. _stepEuler:

stepEuler(self, :ref:`dt`)
--------------------------------
- Method of classes :ref:`Channel` and :ref:`PyPipe_ps`
- Defined in :ref:`channel.cpp` as an implementation of the :ref:`Channel` class
- Takes :ref:`M` Euler time steps of length :ref:`dt` to update the conservation law
- For left state :ref:`q` at i and right state :ref:`q` at i + 1 (where i is a simple index)
- Uses numFlux as a numerical flux
- Returns integer that provides information on how the function was executed


.. _stepRK3_SSP:

stepRK3_SSP(self, :ref:`dt <dt>`)
---------------------------------
- Method of the :ref:`Network <Network>` class
- Defined in :ref:`network.cpp <network.cpp>`
- Takes input parameters self and :ref:`dt <dt>`
- Increments :ref:`channels <channels>` and calls :ref:`EulerStep <EulerStep>`
- Two indexes of i (for :ref:`channels`) and j (for :ref:`Nedges <Nedges>`)
- Returns nothing


.. _stepSourceTerms:

stepSourceTerms(self, :ref:`dt`)
---------------------------------
- Method of :ref:`Channel` objects
- Defined in :ref:`channel.cpp`
- Retrieves source term :ref:`S <SS>` via :ref:`getSourcerTerms`
- Steps the initial term


.. _stepTransportTerms:

stepTransportTerms(self, :ref:`dt`)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- First order upwinding for :ref:`Cl` transport terms
- Returns nothing, simply updates :ref:`Cl0`


.. _update_delta:

update_delta(self, :ref:`rho`, ret0, use_trigger)
---------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`levmar.cpp`
- Updates :ref:`delta`
- Returns ret0 until :ref:`delta` is extremely low
- When :ref:`delta` gets low enough, 1 is returned
- Use trigger sets value :ref:`delta` must be lower than
- If use_trigger equals zero, roundoff regime is activated and :ref:`delta` must approach zero


.. _updateExactRS:

updateExactRS(self, :ref:`q1m`, :ref:`q1p`, :ref:`q2m`, :ref:`q2p`, :ref:`qnew`, :ref:`Pl`, :ref:`Pr`, :ref:`Px`)
---------------------------------
- Method of the :ref:`Cuniform` class
- Defined in :ref:`channel.h`
- Doesn't seem to actually do anything
- Returns zero


.. _update_x:

update_x()
---------------------------------
- Method of the :ref:`Levmar` class
- Defined in :ref:`levmar.cpp`
- Updates :ref:`x` array by adding :ref:`p` per index


.. _w3d_compute_min_max:

w3d_compute_min_max(:ref:`f1d`, :ref:`mn`, :ref:`zmin`, :ref:`zmax`)
-----------------------------------
- Independent function
- Defined in :ref:`file_output.cc`
- Computes the minimum and maximum values of an array given by :ref:`f1d` arguments


.. _w3d_output:

w3d_output(:ref:`filename`, :ref:`f1d`, m, n)
----------------------------------
- Independent function
- Defined in :ref:`file_output.cc`
- Where m is the horizontal grid size and n is the vertical grid size
- Outputs a 2D array in the GNU plot binary format
- The routine treats the array as periodic and repeats the first row and column


.. _w3d_targa_output_surface:

w3d_targa_output_surface(:ref:`filename`, :ref:`f1d`, m, n, :ref:`zmin`, :ref:`zmax`)
----------------------------------
- Independent function
- Defined in :ref:`file_output.cc`
- Outputs a 2D array as a Targa image that can be read as a POV-Ray height field
- The routine treats the array as periodic and repeats the first row and column


.. _writeqToFile:

writeqToFile(self, :ref:`Mi`, :ref:`dt`)
----------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Writes :ref:`q` information to :ref:`M <MM>`/:ref:`Mi` files
- These files are in theory readable by :ref:`smarterputittogether.py`
- Returns 0 if no errors were encountered while writing
- 1 is returned if an error is encountered


.. _writeRIToFile:

writeRIToFile(self, :ref:`dt`, :ref:`sign`)
----------------------------------
- Method of the :ref:`Channel` class
- Defined in :ref:`channel.cpp`
- Writes to a file type readable by GNU plot
- These files are in theory opened in :ref:`smarterputittogether.py`
- Returns 0 if no errors were encountered while writing
- 1 is returned if an error is encountered










