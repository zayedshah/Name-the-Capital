import openpyxl, random, os

base_filePath = r'C:\Users\Zayed\Desktop\Personal_1\Learnings\Python\Games\Working Version\Name the Capital'
abs_filePath = os.path.join(base_filePath, 'Data.xlsx')
wb = openpyxl.load_workbook(abs_filePath)
sheet = wb.get_sheet_by_name('Countries_Capitals')

dictCountriesCapitals = {}
for i in range(2, 199):
    country = sheet.cell(row=i, column=1).value
    capital = sheet.cell(row=i, column=2).value
    dictCountriesCapitals[country] = capital

checkCtry_Chosen_Already = []
for countQuestion in range(10):
    while True:
        randomCountry = random.randint(2, 198)
        if randomCountry not in checkCtry_Chosen_Already:
            checkCtry_Chosen_Already.append(randomCountry)
            break

    country = sheet.cell(row=randomCountry, column=1).value
    print('What is the capital of %s?' % country)
    answer = input()
    correct_answer = dictCountriesCapitals[country]
    if answer == correct_answer:
        print('Correct answer')
    else:
        print('Wrong answer')
        print('The correct answer is: ' + correct_answer)
