! README-file for input data to the SVPPRS optimization model developed for the Xpress solver

! The route input files should have the following format and setup:

nRoutes		: 	<No. of routes> 		! This is the size of the set of pregenerated routes

RouteMaxDur	:	<Duration (in integer days)>	! Specifies the maximum allowed duration for pregenerated routes

nBases		:	<No. of supply bases>		! The number of supply bases used for cargo distribution in the given test instance

nInsts		:	<No. of offshore installations>	! The number of offshore installations present in the given test instance

nDays		:	<Integer days>			! The length of the planning horizon in which cargo demands are specified

TruckDistCalc	:	<Binary number>			! Equals 1 if the test instance involve several bases and truck distribution between bases
							! should be accounted for.

InstTranslation	:	[
<Array of installation IDs>
]							! List of installations included in the test instance (from the full set of installations)


DemandReq	:	[
<nInst x nDays + 1 binary matrix for demands>
]							! Binary matrix specifying on which days each installation requires servicing. An empty column
							! is added at the end (at position {nDays + 1}) in order to give vessels time to return to base

CargoOnRoute	:	[
<Array with dim {1 x nRoutes} and integer values>
]							! This array specifies the cargo quantity loaded onto a PSV before departing on each pregenerated route

SpotAllowed	:	[
<Array with dim {1 x nRoutes} and binary values>
]							! This array specifies whether a route can be sailed by a spot vessel 
							! (equals 1 if start and end base is equal)


DayAtPos	:	[
<Matrix with dim {nInsts x nRoutes} and integer values>
]							! A matrix to keep control on which day each route visits each installation (0 if not visited)


RouteBaseStart	:	[
<Array with dim {1 x nRoutes} and integer values>
]							! Specifies the START BASE for each route in the set of pregenerated routes

RouteBaseEnd	:	[
<Array with dim {1 x nRoutes} and integer values>
]							! Specifies the END BASE for each route in the set of pregenerated routes

RouteStartDays	:	[
<Array with dim {1 x nRoutes} and integer values>
]							! Specifies the START DAY for each route in the set of pregenerated routes

RouteEndDays	:	[
<Array with dim {1 x nRoutes} and integer values>
]							! Specifies the END DAY for each route in the set of pregenerated routes

RouteDurations	:	[
<Array with dim {1 x nRoutes} and integer values>
]							! Specifies the DURATION (in integer days) for each route in the set of pregenerated routes


RouteEmissions	:	[
<Array with dim {1 x nRoutes} and real values>
]							! Specifies the EMISSIONS (in tons of CO2) for each route in the set of pregenerated routes

		