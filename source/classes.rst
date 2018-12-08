Classes
=================================

.. _bc_opt_dh_c:

bc_opt_dh_c
---------------------------------
- Class used as the backbone of :ref:`PyBC_opt_dh`
- Derived from :ref:`Levmar`
- Trial class to implement optimization machinery for adjusting boundary conditions at a single node
- To minimize average pressure gradient
- Inputs:
	:ref:`M <MM>`, :ref:`n <n>`, :ref:`x0`, :ref:`Network` object, :ref:`modetype`, :ref:`T`, and :ref:`whichnode`
- Attributes:
	:ref:`bvals`, :ref:`a0`, :ref:`q0`, :ref:`dt`, :ref:`Vin`, and :ref:`mydelta`
- Methods:
	- :ref:`compute_r <compute_r>`
	- :ref:`compute_J <compute_J>`
	

.. _Channel:

Channel
---------------------------------
- Class used to describe a single pipe or element of pipe network
- Utilized throughout the module
- Holds :ref:`q` of form (:ref:`A <AA>`, :ref:`Q <QQ>`) with methods to update them according to de St. Venant equations
- Can be constructed by :ref:`Channel <Channelfunction>` or destructed by :ref:`~Channel <Channeldestructor>`
- Either :ref:`Cpreiss` or :ref:`Cuniform` based on :ref:`channeltype <cchanneltype>`, has all attributes/methods of specific sub-objects
- Defined in :ref:`channel.cpp` and outlined in :ref:`channel.h`
- Inputs:
	:ref:`Nin`, :ref:`win`, :ref:`Lin`, :ref:`Min`, :ref:`a`, and :ref:`kwin`
- Attributes:
	:ref:`channeltype <channeltype>`, :ref:`w`, :ref:`L <LL>`, :ref:`N <NNN>`, :ref:`n`, :ref:`dx`, :ref:`dry`, :ref:`At`, :ref:`Af`, :ref:`a`, :ref:`Ts`, :ref:`S0`, :ref:`Mr`, :ref:`kn`, :ref:`cmax`, :ref:`kb`, :ref:`kw`, :ref:`q0`, :ref:`q`, :ref:`qhat`, :ref:`q_hist`, :ref:`Cl`, :ref:`Cl0`, :ref:`Clhat`, :ref:`Clhist`, :ref:`P`, :ref:`p_hist`, :ref:`Pnow`, :ref:`bfluxleft`, :ref:`bfluxright`, :ref:`bCll`, and :ref:`bClr`
- Methods:
	- :ref:`idx <idx>`
	- :ref:`idx_t <idx_t>`
	- :ref:`pj <pj>`
	- :ref:`pj_t <pj_t>`
	- :ref:`showVals <showVals>`
	- :ref:`showGeom <showGeom>`
	- :ref:`Channel <Channelfunction>`
	- :ref:`~Channel <Channeldestructor>`
	- :ref:`setq0 <setq0>`
	- :ref:`setq <setq>`
	- :ref:`setC10 <setCl0>`
	- :ref:`stepEuler <setEuler>`
	- :ref:`numFluxHLL <numFluxHLL>`
	- :ref:`physFlux <physFlux>`
	- :ref:`speedsHLL <speedsHLL>`
	- :ref:`speedsRoe <speedsRoe>`
	- :ref:`showp <showp>`
	- :ref:`Eta <Etafunction>`
	- :ref:`HofA <HofA>`
	- :ref:`pbar <pbarfunction>`
	- :ref:`fakehofA <fakehofA>`
	- :ref:`fakeAofh <fakeAofh>`
	- :ref:`AofH <AofH>`
	- :ref:`Cgrav <Cgravfunction>`
	- :ref:`getHydRad <getHydRad>`
	- :ref:`PhiofA <PhiofA>`
	- :ref:`AofPhi <AofPhi>`
	- :ref:`stepSourceTerms <stepSourceTerms>`
	- :ref:`stepTransportTerms <stepTransportTerms>`
	- :ref:`getTheGoddamnVolume <getTheGoddamnVolume>`
	- :ref:`getAveGradH <getAveGradH>`
	- :ref:`getKE <getKE>` 
	- :ref:`getPE <getPE>`
	- :ref:`writeqToFile <writeqToFile>`
	- :ref:`writeRItoFile <writeRItoFile>`
	- :ref:`quickWrite <quickWrite>`
	- :ref:`setClkw <setClkw>`
	- :ref:`getKCl <getKCl>`
	- :ref:`getMassTransCoeff <getMassTransCoeff>`
	- :ref:`min3 <min3>`
	- :ref:`max3 <max3>`

	
.. _Cpreiss:

Cpreiss
---------------------------------
- Brief derived :ref:`Channel` class for Preissman slot geometry
- Where :ref:`channeltype <cchanneltype>` is one
- Inputa:
	:ref:`Nin`, :ref:`win`, :ref:`Lin`, :ref:`Min`, and :ref:`a`
- Attributes:
	:ref:`D`, :ref:`yt`, :ref:`tt`
- Methods:
	- :ref:`showp <showp>`
	- :ref:`Eta <Etafunction>`
	- :ref:`pbar <pbarfunction>`
	- :ref:`HofA <HofA>`
	- :ref:`fakehofA <fakehofA>`
	- :ref:`fakeAofh <fakeAofh>`
	- :ref:`AofH <AofH>`
	- :ref:`Cgrav <Cgravfunction>`
	- :ref:`getHydRad <getHydRad>`
	- :ref:`showGeom <showGeom>`
	- :ref:`findOmega <findOmega>`
	- :ref:`PhiofA <PhiofA>`
	- :ref:`AofPhi <AofPhi>`
	- :ref:`speedsHLL <speedsHLL>`
	- :ref:`speedsRoe <speedsRoe>`
	
	
.. _Cuniform:

Cuniform
---------------------------------
- Brief derived :ref:`Channel` class for pipes with uniform cross sections
- In other words, no Preissman slot
- Where :ref:`channeltype <cchanneltype>` is zero
- Inputs:
	:ref:`Nin`, :ref:`win`, :ref:`Lin`, :ref:`Min`, and :ref:`a`
- Methods:
	- :ref:`showp <showp>`
	- :ref:`Eta <Etafunction>`
	- :ref:`pbar <pbarfunction>`
	- :ref:`HofA <HofA>`
	- :ref:`fakehofA <fakehofA>`
	- :ref:`fakeAofh <fakeAofh>`
	- :ref:`AofH <AofH>`
	- :ref:`Cgrav <Cgravfunction>`
	- :ref:`getHydRad <getHydRad>`
	- :ref:`showGeom <showGeom>`
	- :ref:`speedsHLL <speedsHLL>`
	- :ref:`speedsRoe <speedsRoe>`
	- :ref:`updateExactRS <updateExactRS>`
	- :ref:`PhiofA <PhiofA>`
	- :ref:`AofPhi <AofPhi>`
	

.. _Junction1:	

Junction1
---------------------------------
- Brief class for applying boundary conditions
- Represents the external boundary of a single pipe
- Tied to the :ref:`Channel` object of which the junction is a boundary of
- Inputs:
	:ref:`Channel` object, :ref:`whichend`, :ref:`bvals`, and :ref:`bvaltype`
- Attributes:
	:ref:`N <NNN>`, :ref:`w`, :ref:`reflect`, and :ref:`Clbval`
- Methods:
	- :ref:`setbVal <setbVal>`
	- :ref:`setClbVal <setClbVal>`
	- :ref:`Junction1 <Junction1function>`
	- :ref:`~Junction1 <Junction1destructor>`
	- :ref:`boundaryFluxes <boundaryFluxes>`
	- :ref:`getFlowThrough <getFlowThrough>`

	
.. _Junction2:

Junction2
---------------------------------
- Brief class for applying boundary conditions at a junction
- This junction being one with two :ref:`Channels <Channel>` connected in serial
- Tied to the two :ref:`Channel` objects the junction joins
- Inputs:
	2 :ref:`Channel` objects, :ref:`whichend0`, :ref:`whichend1`, and :ref:`valveopen`
- Attributes:
	:ref:`N0`, :ref:`N1`, :ref:`Ns0`, :ref:`Ns1`, :ref:`dx0`, :ref:`dx1`, :ref:`valvetimes`, and :ref:`offset`
- Methods:
	- :ref:`setValveTimes <setValveTimes>`
	- :ref:`boundaryFluxes <boundaryFluxes>`
	- :ref:`Junction2 <Junction2function>`


.. _Junction3:

Junction3
---------------------------------
- Brief class for applying boundary conditions at a junction
- This junction being one with three connected :ref:`Channels <Channel>`
- Tied to the three :ref:`Channel` objects the junction joins
- Parameters:
	3 :ref:`Channel` objects, :ref:`whichend0`, :ref:`whichend1`, :ref:`whichend2`
- Attributes:
	4 :ref:`Junction2` objects (junctions between all pairs), :ref:`Ns0`, :ref:`Ns1`, :ref:`Ns2` and :ref:`offsets`
- Methods:
	- :ref:`boundaryFluxes <boundaryFluxes>`
	- :ref:`Junction3 <Junction3function>`


.. _Levmar:

Levmar
---------------------------------
- Class for performing a Levenberg-Marguardt optimization
- Defined in :ref:`levmar.cpp`
- Minimizes :ref:`f` with respect to :ref:`r`
- Needed to identify mystery boundary conditions
- Input Dimensions:
	:ref:`m`, :ref:`n`
- Attributes:
	:ref:`x`, :ref:`r`, :ref:`f`, :ref:`df`, :ref:`D`, :ref:`gammaD`
- Methods:
	- :ref:`levmar <levmarfunction>`
	- :ref:`set_init_params <set_init_params>`
	- :ref:`set_dist_mat_ptrs <set_dist_mat_ptrs>`
	- :ref:`set_x <set_x>`
	- :ref:`update_x <update_x>`
	- :ref:`set_gammaD <set_gammaD>`
	- :ref:`compute_diag <compute_diag>`
	- :ref:`chkder <chkder>`
	- :ref:`compute_f <compute_f>`
	- :ref:`compute_g <compute_g>`
	- :ref:`compute_J <compute_J>`
	- :ref:`compute_r <compute_r>`
	- :ref:`dump <dump>`
	- :ref:`solve <solve>`
	- :ref:`check_reduction <check_reduction>`
	- :ref:`check_reduction_roundoff_regime <check_reduction_roundoff_regime>`
	- :ref:`update_delta <update_delta>`
	- :ref:`compute_p2 <compute_p2>`
	- Many more simple value assignment functions detailed in :ref:`levmar.h`


.. _Network:

Network
---------------------------------
- Class holding information about the pipe network
- Utilized and referenced in the :ref:`PyNetwork <PyNetwork>` class
- Conveniently defined in the :ref:`network.cpp <network.cpp>` file
- Has implementations that allow the network to be copied or destructed
- Inputs:
	:ref:`Nnodes <Nnodes>`, :ref:`conn <conn>`, :ref:`Nedges <Nedges>`, :ref:`Ns <Ns>`, :ref:`ws <ws>`, :ref:`Ls <Ls>`, :ref:`S0s <S0s>`, :ref:`Mrs <Mrs>`, :ref:`a0s <a0s>`, :ref:`q0s <q0s>`, :ref:`M <M>`, and :ref:`channeltype <channeltype>`
- Methods:
	- :ref:`EulerStep <EulerStep>`
	- :ref:`stepRK3_SSP <stepRK3_SSP>`
	- :ref:`runForwardProblem <runForwardProblem>`
	- :ref:`getTotalVolume <getTotalVolume>`
	- :ref:`getAveGradH <getAveGradH>`
	- :ref:`getKE <getKE>`
	- :ref:`getPE <getPE>`	


.. _nlEig:

nlEig
---------------------------------
- Class derived from :ref:`Levmar`
- Defined in :ref:`nlEig.cpp`
- Very small but needed for approximations
- Holds a :ref:`Levmar` object of inputs :ref:`n` x :ref:`n`
- Inputs:
	:ref:`n` and :ref:`a`
- Attributes:
	:ref:`amp` and :ref:`dx`
- Methods:
	- :ref:`compute_r <compute_r>`
	- :ref:`compute_J <compute_J>`
	
	
.. _PyBC_opt_dh:

PyBC_opt_dh
---------------------------------
- Class similar to :ref:`PyMystery_BC`
- Defined in :ref:`allthethings.pyx`
- Constructed around an :ref:`bc_opt_dh_c` object
- Required to optimize function of change in :ref:`H` with respect to :ref:`x` at one node
- Inputs:
	:ref:`fi`, :ref:`fc`, :ref:`ndof`, :ref:`x0`, :ref:`whichnode`, :ref:`Vin`, and :ref:`modetype`
- Attributes:
	:ref:`solve_t` and :ref:`w_solve_t`
- Methods:
	- :ref:`solve <solve>`
	- :ref:`dump <dump>`
	- :ref:`compute_f <compute_f>`
	- :ref:`getBCtimeseries <getBCtimeseries>`
	- :ref:`getBCTimeSeries2 <getBCTimeSeries2>`
	

.. _PyNetwork: 

PyNetwork
---------------------------------
- Network class with layout and state information
- Defined in :ref:`allthethings <allthethings.pyx>`
- Set up by :ref:`getTimeSeries` and the conveniently named :ref:`setupNetwork <setupNetwork>`
- Holds an internal :ref:`Network <Network>` object
- Inputs:
	:ref:`fin <fin>`, :ref:`fconfig <fconfig>`, and :ref:`channeltype <channeltype>`
- Attributes:
	:ref:`conn <conn>`, :ref:`Nedges <Nedges>`, :ref:`Nnodes <Nnodes>`, :ref:`Nvar <Nvar>`, :ref:`Ns <Ns>`, :ref:`T <TTT>`, :ref:`M <MM>`, :ref:`nn <nn>`, and :ref:`a <a>`
- Methods:
	- :ref:`runForwardProblem <runForwardProblem>`
	- :ref:`q <qfunction>`
	- :ref:`setIC <setIC>`
	- :ref:`showLayout <showLayout>`
	- :ref:`showCurrentPipeData <showCurrentPipeData>`
	- :ref:`getAveGradH <getAveGradH>`
	- :ref:`getTotalVolume <getTotalVolume>`

	
.. _PyPipe_ps:

PyPipe_ps
---------------------------------
- Takes and gives information on a single pipe
- Defined in :ref:`allthethings <allthethings.pyx>`
- Holds an internal :ref:`Channel <Channel>` object, thus has all methods and attributes of such an object
- Inputs:
	:ref:`N <NNN>`, :ref:`D <D>`, :ref:`L <L>`, :ref:`M <MM>`, and :ref:`a <a>`
- Attributes:
	:ref:`q <q>`, :ref:`q0 <q0>`, :ref:`cmax <cmax>`, :ref:`dx <dx>`, :ref:`Ts <Ts>`, and :ref:`At <At>`
- Methods:
	- :ref:`showGeom <showGeom>`
	- :ref:`stepEuler <stepEuler>`
	- :ref:`PhiofA <PhiofA>`
	- :ref:`AofPhi <AofPhi>`
	- :ref:`Cgrav <Cgrav>`
	- :ref:`HofA <HofA>`
	- :ref:`AofH <AofH>`
	- :ref:`Eta <Etafunction>`
	- :ref:`pbar <pbar>`

	
.. _PyMystery_BC:

PyMystery_BC
---------------------------------
- Optimize to fit unknown boundary conditions to a measured time series of pressure head h
- Defined in :ref:`allthethings <allthethings.pyx>`
- Inputs:
	:ref:`fi <fi>`, :ref:`fc <fc>`, :ref:`ndof <ndof>`, :ref:`x0 <x0>`, :ref:`hdata <hdata>`, :ref:`modetype <modetype>`, :ref:`pj <pj>`, :ref:`xstar <xstar>`, :ref:`whichnode <whichnode>`, :ref:`qfixed <qfixed>`, and :ref:`delay <delay>`
- Attributes:
	:ref:`solve_t <solve_t>`, :ref:`w_solve_t <w_solve_t>`, :ref:`x <x>`, :ref:`r <r>`, :ref:`f <f>`, :ref:`T <TTT>`, :ref:`M <MM>`
- Methods:
	- :ref:`solve <solve>`
	- :ref:`dump <dump>`
	- :ref:`compute_f <compute_f>`
	- :ref:`getBCtimeseries <getBCtimeseries>`

	