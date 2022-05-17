def bmrWomen(weight, height, age):
  bmrF = (10*weight) + (6.25*height) - (5*age) - 161
  return bmrF


def bmrMen(weight, height, age):
  bmrM = (10*weight) + (6.25*height) - (5*age) + 5
  return bmrM


def bmi(weight, height):  
  bmi = 703 * (weight/(height*height))
  return bmi


def bmiCat(bmi):
  if bmi > 30:
    return 'Obese'
  elif bmi <=30 and bmi >=25:
    return 'Overweight'
  elif bmi <=25 and bmi >=18.5:
    return 'Normal'
  else:
    return 'Underweight'
  
  
def bfpM(bmi, age):  
  bfpM = (1.20 * bmi) + (.23 * age) -16.2
  return bfpM


def bfpW(bmi, age):   
  bfpW = (1.20*bmi) + (.23*age) - 5.4
  return bfpW


def bfcW(age, bfpW):
  if age >=20 and age <=40:
    if bfpW <21:
      return 'Underfat'
    elif bfpW >=21 and bfpW <= 33:
      return 'Healthy'
    elif bfpW >= 33 and bfpW <= 39:
      return 'Overweight'
    else:
      return 'Obese'
    
  elif age >= 41 and age <= 60:
    if bfpW <23:
      return 'Underfat'
    elif bfpW >=23 and bfpW <= 35:
      return 'Healthy'
    elif bfpW >= 35 and bfpW <= 40:
      return 'Overweight'
    else:
      return 'Obese'
    
  elif age >= 61 and age <= 79:
    if bfpW <24:
      return 'Underfat'
    elif bfpW >=24 and bfpW <= 36:
      return 'Healthy'
    elif bfpW >= 36 and bfpW <= 42:
      return 'Overweight'
    else:
      return 'Obese'
  
  
def bfcM(age, bfpM):  
  if age >=20 and age <= 40:
    if bfpM <8:
      return 'Underfat'
    elif bfpM >=8 and bfpM <= 19:
      return 'Healthy'
    elif bfpM >= 19 and bfpM <= 25:
      return 'Overweight'
    else:
      return 'Obese'
    
  elif age >= 41 and age <= 60:
    if bfpM <11:
      return 'Underfat'
    elif bfpM >=11 and bfpM <= 22:
      return 'Healthy'
    elif bfpM >= 22 and bfpM <= 27:
      return 'Overweight'
    else:
      return 'Obese'
    
  elif age >= 61 and age <= 79:
    if bfpM <13:
      return 'Underfat'
    elif bfpM >=13 and bfpM <= 25:
      return 'Healthy'
    elif bfpM >= 25 and bfpM <= 30:
      return 'Overweight'
    else:
      return 'Obese'
  
  
def thrLow(age):  
  maxHR = 220 - age
  low = maxHR *.50
  return low 


def thrHigh(age):
  maxHR = 220 - age
  high = maxHR  * .85
  return high
  
  
def main():
  gender = input("What is your gender?  Type 'M' for male, 'F' for female, or 'N' to skip the question: ")
  age = int(input("Input your age: "))
  height = float(input("Input your height in inches: "))
  weight = float(input("Input your weight in pounds: "))

  #Runs if gender question is skipped
  if gender == 'N':
    bmiFinal = bmi(weight, height)
    bmiCategory = bmiCat(bmiFinal)
    targetLow = thrLow(age)
    targetHigh = thrHigh(age)
    print(f"\nYour BMI is {bmiFinal}, which is categorized as {bmiCategory}")
    print(f"Your Target Heart Rate while exercising should be between {targetLow} and {targetHigh} beats per minute.\n")
    
  #Runs if 'F' is chosen as gender  
  elif gender == 'F':
    bmrFinal = bmrWomen(weight, height, age)
    bmiFinal = bmi(weight, height)
    bmiCategory = bmiCat(bmiFinal)
    bfpFinal = bfpW(bmiFinal, age)
    bfcFinal = bfcW(age, bfpFinal)
    targetLow = thrLow(age)
    targetHigh = thrHigh(age)
    print(f"\nYour BMR is {bmrFinal} calories per day")
    print(f"Your BMI is {bmiFinal}, which is categorized as {bmiCategory}")
    print(f"Your BFP is {bfpFinal}%, which is categorized as {bfcFinal}")
    print(f"Your Target Heart Rate while exercising should be between {targetLow} and {targetHigh} beats per minute.\n")
  
  #Runs if 'M' is chosen as gender
  elif gender == 'M':
    bmrFinal = bmrMen(weight, height, age)
    bmiFinal = bmi(weight, height)
    bmiCategory = bmiCat(bmiFinal)
    bfpFinal = bfpM(bmiFinal, age)
    bfcFinal = bfcM(age, bfpFinal)
    targetLow = thrLow(age)
    targetHigh = thrHigh(age)
    print(f"\nYour BMR is {bmrFinal} calories per day")
    print(f"Your BMI is {bmiFinal}, which is categorized as {bmiCategory}")
    print(f"Your BFP is {bfpFinal}%, which is categorized as {bfcFinal}")
    print(f"Your Target Heart Rate while exercising should be between {targetLow} and {targetHigh} beats per minute.\n")
  
  
  
if __name__== "__main__":
  main()
