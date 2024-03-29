# property-matcher
Algorithm to match these properties and search criteria such that each match has a match percentage.

PROBLEM:
Agentdesks has a lot of properties from property sellers and searches requirements from property buyers which get added to a SQL database every day. Every day these multiple properties and search criteria get added through our application by agents. Write an algorithm to match these properties and search criteria as they come in based on 4 parameters such that each match has a match percentage.

The 4 parameters are:
Distance - radius (high weightage)
Budget (high weightage)
Number of bedrooms (low weightage)
Number of bathrooms (Low weightage)
Each match should have a percentage that indicates the quality of the match. Ex: if a property exactly matches a buyers search requirement for all 4 constraints mentioned above, it’s a 100% match.
Each property has these 6 attributes - Id, Latitude, Longitude, Price, Number of bedrooms, Number of bathrooms
Each requirement has these 9 attributes - Id, Latitude, Longitude, Min Budget, Max budget, Min Bedrooms required, Max bedroom reqd, Min bathroom reqd, Max bathroom reqd.
Functional requirements
All matches above 40% can only be considered useful.
The code should scale up to a million properties and requirements in the system.
All corner cases should be considered and assumptions should be mentioned
Requirements can be without a min or a max for the budget, bedroom and a bathroom but either min or max would be surely present.
For a property and requirement to be considered a valid match, distance should be within 10 miles, the budget is +/- 25%, bedroom and bathroom should be +/- 2.
If the distance is within 2 miles, distance contribution for the match percentage is fully 30%
If the budget is within min and max budget, budget contribution for the match percentage is full 30%. If min or max is not given, +/- 10% budget is a full 30% match.
If bedroom and bathroom fall between min and max, each will contribute full 20%. If min or max is not given, match percentage varies according to the value.
The algorithm should be reasonably fast and should be quick in responding with matches for the users once they upload their property or requirement.
