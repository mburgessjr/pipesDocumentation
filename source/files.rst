File Mapping
=================================


.. _allthethings.pyx:

allthethings.pyx
---------------------------------
- The virtual backbone of the module, holds main classes
- Contains:
	- :ref:`Clhist <Clhist>`
	- :ref:`compute_f <compute_f>`
	- :ref:`dump <dump>`
	- :ref:`idx_t <idx_t>`
	- :ref:`getBCtimeseries <getBCtimeseries>`
	- :ref:`getBCTimeSeries2 <getBCTimeSeries2>`
	- :ref:`phist <phist>`
	- :ref:`pressureSpaceSeries <pressureSpaceSeries>`
	- :ref:`pressureTimeSeries <pressureTimeSeries>`
	- :ref:`PyBC_opt_dh <PyBC_opt_dh>`
	- :ref:`PyMystery_BC <PyMystery_BC>`
	- :ref:`PyNetwork <PyNetwork>`
	- :ref:`PyPipe_ps <PyPipe_ps>`
	- :ref:`q <qfunction>`
	- :ref:`qhist <qhist>`
	- :ref:`reset <reset>`
	- :ref:`runForwardProblem <runForwardProblem>`
	- :ref:`setIC <setIC>`
	- :ref:`showCurrentData <showCurrentData>`
	- :ref:`showExternalBoundaries <showExternalBoundaries>`
	- :ref:`showLayout <showLayout>`
	- :ref:`solve <solve>`
	

.. _allthethings.cpp:

allthethings.cpp
---------------------------------
- Cython conversion of :ref:`allthethings.pyx <allthethings.pyx>`
- Holds same things as :ref:`allthethings.pyx`, however in a different language
	

.. _angleview.pov:
	
angleview.pov
---------------------------------
- 3D graphic file
- Holds a created graphic of pipes
- Part of module's output


.. _basic_time_series.h:

basic_time_series.h
---------------------------------
- Holds definition of :ref:`getTimeSeries`
- Contains:
	- :ref:`getTimeSeries <getTimeSeries>`
	

.. _channel.h:

channel.h
---------------------------------
- Defines things needed for :ref:`channel.cpp <channel.cpp>`
- This chiefly concerns the :ref:`Channel` class and associated method functions and attribute variables
- To be included where :ref:`Channel` objects and other contained definitions must be utilized
- Contains many of the full definitions of implementations of :ref:`Cuniform` as one line functions
- Exclusively contains definitions for:
	- :ref:`AofH <AofH>`
	- :ref:`AofPhi <AofPhi>`
	- :ref:`Cgrav <Cgravfunction>`
	- :ref:`Eta <Etafunction>`
	- :ref:`fakeAofh <fakeAofh>`
	- :ref:`fakehofA <fakehofA>`
	- :ref:`getHydRad <getHydRad>`
	- :ref:`HofA <HofA>`
	- :ref:`idx <idx>`
	- :ref:`pbar <pbar>`
	- :ref:`PhiofA <PhiofA>`
	- :ref:`pj <pj>`
	- :ref:`pj_t <pj_t>`
	- :ref:`updateExactRS <updateExactRS>`


.. _channel.cpp:

channel.cpp
---------------------------------
- Contains many definitions concerning the object of individual pipes themselves
- Outlines the :ref:`Channel` class and associated methods and attributes
- Establishes the classes :ref:`Junction1`, :ref:`Junction2`, and :ref:`Junction3` amongst other things
- All below declared in :ref:`channel.h`
- Contains:
	- :ref:`AofH <AofH>`
	- :ref:`AofPhi <AofPhi>`
	- :ref:`boundaryFluxes <boundaryFluxes>`
	- :ref:`Cgrav <Cgravfunction>`
	- :ref:`Channel <Channel>`
	- :ref:`Channel constructor <Channelfunction>`
	- :ref:`~Channel <Channeldestructor>`
	- :ref:`Eta <Etafunction>`
	- :ref:`fakeAofh <fakeAofh>`
	- :ref:`fakehofA <fakehofA>`
	- :ref:`findOmega <findOmega>`
	- :ref:`getHydRad <getHydRad>`
	- :ref:`getFlowThrough <getFlowThrough>`
	- :ref:`getKCl <getKCl>`
	- :ref:`getMassTransCoeff <getMassTransCoeff>`
	- :ref:`HofA <HofA>`
	- :ref:`Junction1 <Junction1>`
	- :ref:`~Junction1 <Junction1destructor>`
	- :ref:`Junction2 <Junction2>`
	- :ref:`Junction3 <Junction3>`
	- :ref:`numFluxHLL <numFluxHLL>`
	- :ref:`PhiofA <PhiofA>`
	- :ref:`physFlux <physFlux>`
	- :ref:`quickWrite <quickWrite>`
	- :ref:`setCl0 <setCl0>`
	- :ref:`setClbVal <setClbVal>`
	- :ref:`setClkw <setClkw>`
	- :ref:`setq <setq>`
	- :ref:`setq0 <setq0>`
	- :ref:`setValveTimes <setValveTimes>`
	- :ref:`showGeom <showGeom>`
	- :ref:`showVals <showVals>`
	- :ref:`speedsHLL <speedsHLL>`
	- :ref:`speedsRoe <speedsRoe>`
	- :ref:`stepEuler <stepEuler>`
	- :ref:`stepSourceTerms <stepSourceTerms>`
	- :ref:`stepTransportTerms <stepTransportTerms>`
	- :ref:`writeqToFile <writeqToFIle>`


.. _channel_old.h:

channel_old.h
---------------------------------
- Old and no longer used file
- Previously held the place of current :ref:`channel.h`


.. _chebyshevlite.h:

chebyshevlite.h
---------------------------------
- Header file with a few function definitions
- These definitions are Chebyshev routines
- Contains:
	- :ref:`getChebNodes <getChebNodes>`
	- :ref:`ChebEval <ChebEval>`


.. _driver.cpp:

driver.cpp
---------------------------------
- Runs some data
- More specifically, sets some stage_sizes and loads a curve


.. _f_blas_lapack.h:

f_blas_lapack.h
---------------------------------
- Defines a great many non-scalar operations
- These are things from the dot products of two variables, a sum, or normalization
- From linear algebra package


.. _file_output.hh:

file_output.hh
---------------------------------
- Outlines functions defined explicitly in :ref:`file_output.cc`
- More so, describes the purpose and functionality of these functions via notes
- To be included where these functions are needed


.. _file_output.cc:

file_output.cc
---------------------------------
- Defines the functions needed to write the output of the module to files
- Ultimately exports 2D array to Targa file
- Contains:
	- :ref:`w3d_compute_min_max <w3d_compute_min_max>`
	- :ref:`w3d_output <w3d_output>`
	- :ref:`w3d_targa_output_surface <w3d_targa_output_surface>`
	

.. _globals.h:

globals.h
---------------------------------
- Simple header file defining global constants
- Specfically :ref:`g <g>`, :ref:`pi`, and :ref:`m_to_psi`
- To be included in files where these values are needed



.. _justrunit.cpp:

justrunit.cpp
---------------------------------
- Tests the module and records things about simulation
- Sort of a work in progress
- It is noted that more tests should be included to the file
- Specfically, making sure input and output match


.. _lapack.h:

lapack.h
---------------------------------
- Defines a great many routines for nonscalar operations
- This includes matrix multiplication and replacement of variables
- Required to be included in many other functions



.. _levmar.h:

levmar.h
---------------------------------
- Outlines the :ref:`Levmar` class
- Also contains many definitions of simple one-line functions
- These functions are mostly methods of the :ref:`Levmar` class that simply set values to a variable
- To be included where :ref:`Levmar` is needed


.. _levmar.cpp:

levmar.cpp
---------------------------------
- Defines the :ref:`Levmar` class
- Explicitly defines most functions that are a method of the :ref:`Levmar` class
- Contains:
	- :ref:`check_reduction <check_reduction>`
	- :ref:`check_reduction_roundoff_regime <check_reduction_roundoff_regime>`
	- :ref:`chkder <chkder>`
	- :ref:`compute_diag <compute_diag>`
	- :ref:`compute_f <compute_f>`
	- :ref:`compute_g <compute_g>`
	- :ref:`compute_J <compute_J>`
	- :ref:`compute_p2 <compute_p2>`
	- :ref:`compute_r <compute_r>`
	- :ref:`dump <dump>`
	- :ref:`Levmar <Levmar>`
	- :ref:`set_dist_mat_ptrs <set_dist_mat_ptrs>`
	- :ref:`set_init_params <set_init_params>`
	- :ref:`set_gammaD <set_gammaD>`
	- :ref:`set_x <set_x>`
	- :ref:`solve <solve>`
	- :ref:`update_delta <update_delta>`
	- :ref:`update_x <update_x>`


.. _libcla.c:

libcla.c
---------------------------------
- Uses linear alegbra package for matrix computation
- This is needed mainly for :ref:`Levmar` approximation objects


.. _mp_mat.h:

mp_mat.h
---------------------------------
- Outlines functions to be explicitly defined in :ref:`mp_mat.cpp`
- To be included where these functions are needed


.. _mp_mat.cpp:

mp_mat.cpp
---------------------------------
- Contains explicit definitions for many short, computational functions
- Can normalize a vector, copy variables, and more


.. _mp_mat_aux.cpp:

mp_mat_aux.cpp
---------------------------------
- Defines more linear algebra and vector operations


.. _mp_mat_double.cpp:

mp_mat_double.cpp
---------------------------------
- Defines more linear algebra and vector operations


.. _network.h:

network.h
---------------------------------
- Outlines things needed for :ref:`network.cpp <network.cpp>`
- To be included where class is utilized

.. _network.cpp:

network.cpp
---------------------------------
- Defines methods and attributes of :ref:`Network` class
- Contains:
	- :ref:`EulerStep <EulerStep>`
	- :ref:`getAveGradH <getAveGradH>`
	- :ref:`getKE <getKE>`
	- :ref:`getPE <getPE>`
	- :ref:`getTheGoddamnVolume <getTheGoddamnVolume>`
	- :ref:`getTotalVolume <getTotalVolume>`
	- :ref:`Network <Network>`
	- :ref:`runForwardProblem <runForwardProblem>`
	- :ref:`stepRK3_SSP <stepRK3_SSP>`


.. _newton.h:

newton.h
---------------------------------
- Defines :ref:`Newton` function
- Included where function is needed
- Equivalent to :ref:`newton.cpp` file


.. _newton.cpp:

newton.cpp
---------------------------------
- Defines :ref:`Newton` function
- Equivalent to :ref:`newton.cpp` file


.. _nlEig.cpp:

nlEig.cpp
---------------------------------
- Defines the :ref:`nlEig` class explicitly
- Contains:
	- :ref:`compute_J <compute_J>`
	- :ref:`compute_r <compute_r>`
	- :ref:`nlEig <nlEig>`

	
.. _optdetritus.h:

optdetritus.h
---------------------------------
- Outlines the :ref:`bc_opt_dh_c` class
- Contains:
	- :ref:`compute_J <compute_J>`
	- :ref:`compute_r <compute_r>`


.. _optimizeit.h:

optimizeit.h
---------------------------------
- Outlines things to be defined more explicitly in :ref:`optimizeit.cpp`
- To be included where these functions and classes are needed


.. _optimizeit.cpp:

optimizeit.cpp
---------------------------------
- Defines classes for optimization via Levenburg-Marguardt
- Declares many classes derived from :ref:`Levmar`
- Contains:
	- :ref:`bc_opt_dh_c <bc_opt_dh_c>`
	- :ref:`compute_r <compute_r>`
	- :ref:`compute_J <compute_J>`


.. _real_def.h:

real_def.h
---------------------------------
- Declares a few variables and functions
- Centered around the value Epsilon


.. _ridders.h:

ridders.h
---------------------------------
- Defines two large functions called brent and ridders
- Calls new functions object and runs diagnostics


.. _setup.py:

setup.py
---------------------------------
- Used and ran to initially install the module


.. _setupandrun.h:

setupandrun.h
---------------------------------
- Outlines the functions to be defined in :ref:`setupandrun.cpp`
- To be included where these functions are needed


.. _setupandrun.cpp:

setupandrun.cpp
---------------------------------
- Very important document
- Defines functions that allow the initial setup of the main network
- Followed by functions that write an output to Targa and text files respectively
- Contains:
	- :ref:`getTimeSeries <getTimeSeries>`


.. _smarterputittogether.py:

smarterputittogether.py
---------------------------------
- Reads in data produced by functions in :ref:`setupandrun.cpp`
- Uses this data to put together a colored graphical output


.. _steady_states.py:

steady_states.py
---------------------------------
- Creates pipe object for constant inputs


.. _str_double.h:

str_double.h
---------------------------------
- Outlines functions to be defined in :ref:`str_double.cpp`


.. _str_double.cpp:

str_double.cpp
---------------------------------
- Defines two smalls simple functions
- The latter of which literally just maps a string type to a real number


.. _test_dgesvd.cpp:

test_dgesvd.cpp
---------------------------------
- Tests dgesvd
- Dgesvd is a function used in :ref:`lapack.h` for matrix calculations


.. _test_levmar.cpp:

test_levmar.cpp
---------------------------------
- Tests :ref:`Levmar` class
- Uses random sample values to optimize


.. _testcython.py:

testcython.py
---------------------------------
- Tests Cython usage
- Calls classes and prints an evaluation of performance


.. _top.h:

top.h
---------------------------------
- Defines some universal constants such root 2 and 2 pi
- Also outlines a few simple structures and classes


.. _topview.pov:

topview.pov
---------------------------------
- Top view of output
- Point of view grapical written file


.. _writeit.py:

writeit.py
---------------------------------
- Holds utlities fro dealing with input and configuration files
- Has the power to rewrite these files


