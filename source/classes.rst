Classes
=================================


.. _Channel:

Channel
---------------------------------




.. _Junction1:	

Junction1
---------------------------------




.. _Junction2:

Junction2
---------------------------------




.. _Junction3:

Junction3
---------------------------------




.. _Levmar:

Levmar
---------------------------------




.. _Network:

Network
---------------------------------
- Class holding information about the pipe network
- Utilized and referenced in the :ref:`PyNetwork <PyNetwork>` class
- Conveniently defined in the :ref:`network <network.cpp>` file
- Has implementations that allow the network to be copied or destructed
- Requires input parameters:
	:ref:`Nnodes <Nnodes>`, :ref:`conn <conn>`, :ref:`Nedges <Nedges>`, :ref:`Ns <Ns>`, :ref:`ws <ws>`, :ref:`Ls <Ls>`, :ref:`S0s <S0s>`, :ref:`Mrs <Mrs>`, :ref:`a0s <a0s>`, :ref:`q0s <q0s>`, :ref:`M <M>`, and :ref:`channeltype <channeltype>`
- Has methods:
	:ref:`EulerStep <EulerStep>`, :ref:`stepRK3_SSP <stepRK3_SSP>`, :ref:`runForwardProblem <runForwardProblem>`, :ref:`getTotalVolume <getTotalVolume>`, :ref:`getAveGradH <getAveGradH>`, :ref:`getKE <getKE>`, and :ref:`getPE <getPE>`	
	

.. _PyNetwork: 

PyNetwork
---------------------------------
- Network class with layout and state information
- Defined in :ref:`allthethings <allthethings.pyx>`
- Set up by :ref:`getTimeSeries` and the conveniently named :ref:`setupNetwork <setupNetwork>`
- Holds an internal :ref:`Network <Network>` object
- Requires input parameters:
	:ref:`fin <fin>`, :ref:`fconfig <fconfig>`, and :ref:`channeltype <channeltype>`
- Holds attributes:
	:ref:`conn <conn>`, :ref:`Nedges <Nedges>`, :ref:`Nnodes <Nnodes>`, :ref:`Nvar <Nvar>`, :ref:`Ns <Ns>`, :ref:`T <T>`, :ref:`M <M>`, :ref:`nn <nn>`, and :ref:`a <a>`
- Has methods:
	:ref:`runForwardProblem <runForwardProblem>`, :ref:`q <qfunction>`, :ref:`setIC <setIC>`, :ref:`showLayout <showLayout>`, :ref:`showCurrentPipeData <showCurrentPipeData>`, :ref:`getAveGradH <getAveGradH>`, and :ref:`getTotalVolume <getTotalVolume>`

	
.. _PyPipe_ps:

PyPipe_ps
---------------------------------
- Takes and gives information on a pipe
- Defined in :ref:`allthethings <allthethings.pyx>`
- Holds an internal :ref:`Channel <Channel>` object
- Requires input parameters:
	:ref:`N <N>`, :ref:`D <D>`, :ref:`L <L>`, :ref:`M <M>`, and :ref:`a <a>`
- Holds attributes:
	:ref:`q <q>`, :ref:`q0 <q0>`, :ref:`cmax <cmax>`, :ref:`dx <dx>`, :ref:`Ts <Ts>`, and :ref:`At <At>`
- Has methods:
	:ref:`setGeom <setGeom>`, :ref:`stepEuler <stepEuler>`, :ref:`PhiofA <PhiofA>`, :ref:`AofPhi <AofPhi>`, :ref:`Cgrav <Cgrav>`, :ref:`HofA <HofA>`, :ref:`AofH <AofH>`, :ref:`Eta <Eta (the function)>`, and :ref:`pbar <pbar>`

	
.. _PyMystery_BC:

PyMystery_BC
---------------------------------
- Optimize to fit unknown boundary conditions to a measured time series of pressure head h
- Defined in :ref:`allthethings <allthethings.pyx>`
- Requires input parameters:
	:ref:`fi <fi>`, :ref:`fc <fc>`, :ref:`ndof <ndof>`, :ref:`x0 <x0>`, :ref:`hdata <hdata>`, :ref:`modetype <modetype>`, :ref:`pj <pj>`, :ref:`xstar <xstar>`, :ref:`whichnode <whichnode>`, :ref:`qfixed <qfixed>`, and :ref:`delay <delay>`
- Holds attributes:
	:ref:`solve_t <solve_t>`, :ref:`w_solve_t <w_solve_t>`, :ref:`x <x>`, :ref:`r <r>`, :ref:`f <f>`, :ref:`T <T>`, :ref:`M <M>`
- Has methods:
	:ref:`solve <solve>`, :ref:`dump <dump>`, :ref:`compute_f <compute_f>`, and :ref:`getBCtimeseries <getBCtimeseries>`

	