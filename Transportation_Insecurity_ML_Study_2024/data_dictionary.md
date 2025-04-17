# Getting important features

This census dataset has about 3000 columns, across n categories. 

To reduce dimensionality, we start with either (1) one-two representative variable for each category that is expected to not be correlated with transportation and (2) for categories that are expected to be very correlated, we take several variables. 

## Categories and associated variables to be included

Housing Unit Characteristics
* YRBUILT - Year Structure Built, integer
* FOUNDTYPE - Foundation type
    * Single family: FOUNDTYPE IN (1,2,3,4)
    * Manufactured/mobile home: FOUNDTYPE IN (5,6,7,8)
    * Other: FOUNDTYPE = 9 

General Housing
* BLD - Units in Structure
    * Single detached: BLD = 2
    * Single attached: BLD = 3
    * Low density (2-9): BLD IN (4,5,6)
    * Mid density (10-19): BLD = 7
    * High density (20+): BLD IN (8, 9) 
    * Manufactured/mobile: BLD = 1
    * Other: BLD = 10 

Rooms, Size, Amenities
* UNITSIZE - Square footage of unit 
    * <500: 1
    * 500 - 749: 2
    * 750 - 999: 3
    * 1000 - 1499: 4
    * 1500 - 1999: 5
    * 2000 - 2499: 6
    * 2500 - 2999: 7
    * 3000 - 3999: 8 
    * 4000+ : 9 

Heating, AC, Appliances
* HEATFUEL - Main house heating fuel 
    * Electricity: 1
    * Piped gas: 2
    * Bottled gas: 3
    * Fuel oil: 4
    * Kerosene: 5
    * Coal/coke: 6
    * Wood: 7
    * Solar: 8 
    * Other : 9 

Plumbing, Water, Sewage
* WATSOURCE - Primary source of water
    * Public/private system: 1
    * Individual well: 2
    * Other: 3

Housing Quality
* ADEQUACY - Housing adequacy 
    * Severely inadequate: 3
    * Moderately inadequate: 2
    * Adequate: 1

Migration (Reasons for leaving previous residence)
* MOVWHY
    * Financial/goverment : 1
    * Natural disaster: 2
* RMJOB (binary) - new job 
* RMOWNHH (binary) - form own household
* RMFAMILY (binary) - closer to family
* RMCHANGE (binary) - Change in household
* RMCOMMUTE (binary) - Reduce commuting time
* RMHOME (binary) - Larger home desired
* RMCOSTS (binary) - Reduced housing costs
* RMHOOD (binary) - Wanted more desirable neighbourhood
* RMOTHER (binary) - Other
* If any of the above is outside range: Not reported

Neighbourhood Search 
* SEARCHSTOP != 'N' & NRATE: Comparison to previous neighbourhood
    * Better neighbourhood - 1
    * Worse neighbourhood - 2
    * About the same - 3
    * Same neighbourhood - 4

Demographics
* HHRACE - Race origin 
* HHGRAD - Educational attainment 
* HHCITSHP - Citizen of united states 
* NUMPEOPLE - Number of people 
* MULTIGEN - Multigenerational household 

Disabilities
* HHDISH - Households with disabled persons
    * With a disabled person - 1
    * Without a disabled person - 2

Income
* HINCP - Household income 

Housing Costs
* TOTHCAMPT - Monthly Total housing costs 

Value, Price
* MARKETVAL - Market value of home 


Rent Sub & Rent Mgmt
* RENTCNTRL
    * Controlled - 1
    * No rent control - 2
* HUDSUB
    * Public housing - 1
    * Voucher - 2
    * Privately owned subsizied housing - 1
    * No government rental assisstance - 3
    
Neighbourhoods
* NHQSCHOOL - Has good schools
    * Agree - 1
    * Disagree - 2
* NHQPUBTRN - Has good public transportation 
    * Agree - 1
    * Disagree - 2
* RATINGNH - Overall opinion of present home (from 1 to 10) 

Disaster Prep
* DPEVVEHIC - Evacuation vehicle available
    * Yes - 1
    * No - 2

Delinquent Payments
* MORTSTAT in (2,3,4,5) & DBMISSMORT
    * On time - 5
    * Missed or late - 1,2,3,4

Commuting
* COMDAYS - Number of days commute to work 
* DRIVEALL - Number of days driven to work
* DIST - Distance to work 
* BUS - Commute included bus
* SUBWAY - Commute included subwad
* VAN - Commute included van 
* COMTYPE - Whether method was multimodal

Annual Commuting Costs
* COMCOST - annual commuting costs
* SUBSIDY - employer subsidies for commuting 

