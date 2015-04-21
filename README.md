# Problem Set 1 
# Name: Małgorzata Metryka
# Collaborators: Natalia Prósińska
# Time Spent: 3h 

initBal = float(input('Enter the outstanding balance on your credit card: '))
annualRate = float(input('What is your annual percentage rate (as a decimal, i.e. 18% is .18): '))
minPayRate = float(input('Enter your minimum monthly payment rate (as a decimal, i.e. 2% is .02): '))

monthlyRate = annualRate/12

numMonths = 1
totalPaid = 0

while numMonths <= 12:

   minPayment = round(minPayRate * initBal,2)
   totalPaid += minPayment

   interestPaid = round(monthlyRate * initBal,2)

   principalPaid = minPayment - interestPaid

   initBal -= principalPaid

   print ('Month:, ', numMonths)
   print ('Minimum monthly payment amount: $', minPayment)
   print ('Remaining balance: $', initBal)

   numMonths += 1

print ('RESULT')
print ('Total amount paid: $', totalPaid)
print ('Remaining balance: $', initBal)
