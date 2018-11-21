File Mapping
=================================


.. _allthethings.pyx:

allthethings.pyx
---------------------------------
- The virtual backbone of the module, holds main classes
- Contains:
	- :ref:`Clhist <Clhist>`
	- :ref:`idx_t <idx_t>`
	- :ref:`phist <phist>`
	- :ref:`pressureSpaceSeries <pressureSpaceSeries>`
	- :ref:`pressureTimeSeries <pressureTimeSeries>`
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
	

.. _allthethings.cpp:

allthethings.cpp
---------------------------------
- Cython conversion of :ref:`allthethings.pyx <allthethings.pyx>`
	

.. _angleview.pov:
	
angleview.pov
---------------------------------



.. _basic_time_series.h:

basic_time_series.h
---------------------------------



.. _channel.h:

channel.h
---------------------------------
- Defines things needed for :ref:`channel.cpp <channel.cpp>`


.. _channel.cpp:

channel.cpp
---------------------------------
- Holds main algorithm and many computational definitions
- Contains:
	- :ref:`boundaryFluxes <boundaryFluxes>`
	- :ref:`getKCl <getKCl>`
	- :ref:`HofA <HofA>`
	- :ref:`setCl0 <setCl0>`
	- :ref:`setClkw <setClkw>`
	- :ref:`setValveTimes <setValveTimes>`


.. _channel_old.h:

channel_old.h
---------------------------------



.. _chebyshevlite.h:

chebyshevlite.h
---------------------------------



.. _cython_flags.sh:

cython_flags.sh
---------------------------------



.. _driver.cpp:

driver.cpp
---------------------------------



.. _f_blas_lapack.h:

f_blas_lapack.h
---------------------------------



.. _file_output.hh:

file_output.hh
---------------------------------



.. _file_output.cc:

file_output.cc
---------------------------------



.. _globals.h:

globals.h
---------------------------------
- Defines constants gravitational acceleration, pi, etc.



.. _justrunit.cpp:

justrunit.cpp
---------------------------------



.. _lapack.h:

lapack.h
---------------------------------



.. _levmar.h:

levmar.h
---------------------------------



.. _levmar.cpp:

levmar.cpp
---------------------------------



.. _libcla.c:

libcla.c
---------------------------------



.. _mp_mat.h:

mp_mat.h
---------------------------------



.. _mp_mat.cpp:

mp_mat.cpp
---------------------------------



.. _mp_mat_aux.cpp:

mp_mat_aux.cpp
---------------------------------



.. _mp_mat_double.cpp:

mp_mat_double.cpp
---------------------------------



.. _network.h:

network.h
---------------------------------
- Defines things needed for :ref:`network.cpp <network.cpp>`



.. _network.cpp:

network.cpp
---------------------------------
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



.. _newton.cpp:

newton.cpp
---------------------------------



.. _nEig.cpp:

nlEig.cpp
---------------------------------



.. _optdetritus.h:

optdetritus.h
---------------------------------



.. _optimizeit.h:

optimizeit.h
---------------------------------



.. _optimizeit.cpp:

optimizeit.cpp
---------------------------------



.. _real_def.h:

real_def.h
---------------------------------



.. _ridders.h:

ridders.h
---------------------------------



.. _setup.py:

setup.py
---------------------------------
- Used and ran to initially install the module



.. _setupandrun.h:

setupandrun.h
---------------------------------



.. _setupandrun.cpp:

setupandrun.cpp
---------------------------------



.. _smarterputittogether.py:

smarterputittogether.py
---------------------------------



.. _steady_states.py:

steady_states.py
---------------------------------



.. _str_double.h:

str_double.h
---------------------------------



.. _str_double.cpp:

str_double.cpp
---------------------------------



.. _test_dgesvd.cpp:

test_dgesvd.cpp
---------------------------------


.. _test_levmar.cpp:

test_levmar.cpp
---------------------------------


.. _testcython.py:

testcython.py
---------------------------------
- Tests Cython


.. _top.h:

top.h
---------------------------------



.. _topview.pov:

topview.pov
---------------------------------



.. _writeit.py:

writeit.py
---------------------------------



