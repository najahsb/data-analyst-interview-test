## Answer

* Under 20 - 1000 customers
* 20 to 25 - 0 customers
* 31 to 35 - 0 customers
* 36 to 40 - 0 customers
* 41 to 45 - 0 customers
* 46 to 50 - 0 customers
* Above 50 - 0 customers

## Explanation 
Generate=Factory.create(Age)
data[['first_name','last_name','email','date_of_birth','country_code','create_at','last_login_at']]
for i in range (1,1001)
data append([
generator.first_name(),
generator.last_name(),
generator.email(),
generator.date_of_birth(),
generator.country_code(),
generator.created_at(),
generator.last_login_at(),
])
Dim intYears, AgeYears as Integer
intYears= Year(Now)-Year(date_of_birth)
if Date Serial (Year(Now),Month(date_of _birth),Day(date_of_birth))>Now  Then
Subtract a year if birthday has not arrived this year,
intYears=intYears-1
return intYear
AgeYears=intYears
return AgeYears

Dim intUnder_20, int20_to_25, int26_to_30, int31_to_35, int36_to_40, int41_to_45, int46_to_50, intAbove_50 as integer
intUnder_20= Count(AgeYears<20)
int20_to_25 = Count(20<AgeYears<=25)
int26_to_30 = Count(26<AgeYears<=30)
int31_to_35 = Count(31<AgeYears<=35)
int36_to_40 = Count(36<AgeYears<=40)
int41_to_45 = Count(41<AgeYears<=45)
int46_to_50 = Count(46<AgeYears<=50)
intAbove_50 = Count(AgeYears>50)

End Function

Other than that(option), use excel (Birth date = column E)
Create a column next to birth date name it as date now (column F). Add another column name as Age (Column G)
To calculate age of each customer, Column G =ROUNDDOWN((F1-E1)/365.25,0) , drag down to the very last data
To count number of customer according to range of age =
for <20 =COUNTIF($I$1:$I$1000,"<"&H1002) (H1002=20)
20 to 25 =COUNTIFS($I$1:$I$1000,"<"&F1003,$I$1:$I$1000,">="&H1003) (F1003 = 20, H1003=25)
31 to 35 =COUNTIFS($I$1:$I$1000,"<"&F1004,$I$1:$I$1000,">="&H1004) (F1004 = 31, H1004=35)
36 to 40 =COUNTIFS($I$1:$I$1000,"<"&F1005,$I$1:$I$1000,">="&H1005)(F1005 = 36, H1005=40)
41 to 45 =COUNTIFS($I$1:$I$1000,"<"&F1006,$I$1:$I$1000,">="&H1006)(F1006 = 41, H1006=45)
46 to 50 =COUNTIFS($I$1:$I$1000,"<"&F1007,$I$1:$I$1000,">="&H1007)(F1007 = 46, H1007=50)
Above 50 =COUNTIF($I$1:$I$1000,">"&H1008) (H1008=50)


Other analysis can come out, for example:
i) Country analysis : How many customer according country, analyse which country have the most number of customer
ii) FV MemberSince Analysis : Analyse since when the customers sign up as member (FV account). Come out with number of customers who have been with FV for 5-4 years, 4-3 years, 3-2 years, 2-1 years.
iii) Hot viewing analysis: Count the most favourite time viewing website by customers. 

najah-answer.
