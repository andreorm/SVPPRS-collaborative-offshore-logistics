! ------------------- READ INSTRUCTIONS BEFORE SOLVING!! -------------------------


! This model is used for solving the supply vessel planning problem with resource sharing
! (SVPPRS) used for evaluating the emission reduction potential from increased levels of 
! collaboration among operators in offshore logistics sharing a combined fleet of supply vessels.

! Author: Andreas Breivik Ormevik
! Developed 2023-2025

! Requires the following input files - READ CORRESPONDING README-FILES BEFORE SOLVING!

	! 1) The ROUTE INPUT file containing all the relevant information about #installations, #bases, demands and generated routes used to create weekly schedules
	! 2) The fleet size file controlling settings for the available fleet: Number of vessels, and the day of the planning horizon in which the vessels become available, and from which base
	! 3) Solver settings file, containing details on solver settings (acceptable optimization gap, max solution time) and also parameters related to 

! NOTE THE FOLLOWING: The route input files and this model are both developed to handle
! flexibility in delivery days (+/- 1 day after/before the initially requested day), 
! but for the computational study presented in the paper, only static delivery days are considered.


! In order to solve the problem for various sharing configurations, the correct input (indicated by the CASE NUMBER)
! must be ensured. Case 1 = No sharing, Case 2 = Operator sharing, Case 3 = Base sharing, Case 4 = Full sharing.
! ALSO REMEMBER TO UPDATE FLEET SIZES BY SELECTING THE CORRECT FLEET INPUT FILE!