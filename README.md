import pandas as pd
import matplotlib.pyplot as plt

print('\nTYPES OF GRAPHS- \n1.TOTAL POPULATION \n2.DECADEL POPULATION GROWTH RATE \n3.POPULATION DENSITY')
choice2 = int(input('enter the choice-'))

if choice2 == 1:
    print('\n---------TOTAL POPULATION---------')
    data1 = {
        "India / State/ Union Territory": [
             "Andhra Pradesh", "Arunachal Pradesh", "Assam", "Bihar", "Chhattisgarh", "Goa", "Gujarat",
            "Haryana", "Himachal Pradesh", "Jammu & Kashmir", "Jharkhand", "Karnataka", "Kerala", "Madhya Pradesh",
            "Maharashtra", "Manipur", "Meghalaya", "Mizoram", "Nagaland", "Odisha", "Punjab", "Rajasthan",
            "Sikkim", "Tamil Nadu", "Telangana", "Tripura", "Uttarakhand", "Uttar Pradesh", "West Bengal",
            "Andaman & Nicobar Island", "Chandigarh", "Dadra & Nagar Haveli", "Daman & Diu", "Delhi",
            "Lakshadweep", "Puducherry"
        ],
        "Population - 2011": [
             49386799, 1383727, 31205576, 104099452, 25545198, 1458545, 60439692, 25351462,
            6864602, 12541302, 32988134, 61095297, 33406061, 72626809, 112374333, 2855794, 2966889,
            1097206, 1978502, 41974218, 27743338, 68548437, 610577, 72147030, 35193978, 3673917,
            10086292, 199812341, 91276115, 380581, 1055450, 343709, 243247, 16787941, 64473, 1247953
        ]
    }

    df1 = pd.DataFrame(data1)

    plt.figure(figsize=(12, 10))
    plt.bar(df1["India / State/ Union Territory"], df1["Population - 2011"], color='red')
    plt.title('Population - 2011 by India / State/ Union Territory')
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Population - 2011')
    plt.xticks(rotation=90)
    plt.tight_layout()

    plt.show()
    print('\n')

if choice2 == 2:
    print('\n---------DECADEL POPULATION GROWTH RATE---------')
    data2 = {
        "India / State/ Union Territory": [
            "INDIA", "Andhra Pradesh", "Arunachal Pradesh", "Assam", "Bihar", "Chhattisgarh", "Goa", "Gujarat",
            "Haryana", "Himachal Pradesh", "Jammu & Kashmir", "Jharkhand", "Karnataka", "Kerala", "Madhya Pradesh",
            "Maharashtra", "Manipur", "Meghalaya", "Mizoram", "Nagaland", "Odisha", "Punjab", "Rajasthan",
            "Sikkim", "Tamil Nadu", "Telangana", "Tripura", "Uttarakhand", "Uttar Pradesh", "West Bengal",
            "Andaman & Nicobar Island", "Chandigarh", "Dadra & Nagar Haveli", "Daman & Diu", "Delhi",
            "Lakshadweep", "Puducherry"
        ],
        "Decadal Population Growth Rate - 2001-2011": [
            17.7, 9, 26, 17.1, 25.4, 22.6, 8.2, 19.3, 19.9, 12.9, 23.6, 22.4, 15.6, 4.9, 20.3, 16, 31.8,
            27.9, 23.5, -0.6, 14, 13.9, 21.3, 12.9, 15.6, 13.6, 14.8, 18.8, 20.2, 13.8, 6.9, 17.2, 55.9,
            53.8, 21.2, 6.3, 28.1
        ]
    }

    df2 = pd.DataFrame(data2)

    plt.figure(figsize=(12, 6))

    plt.plot(df2["India / State/ Union Territory"], df2["Decadal Population Growth Rate - 2001-2011"], marker='o', linestyle='-', color='red')
    plt.xticks(rotation=90)
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Decadal Population Growth Rate - 2001-2011')
    plt.title('Decadal Population Growth Rate - 2001-2011 by State/Union Territory')
    plt.grid(True)
    plt.tight_layout()

    plt.show()
    print

if choice2 == 3:
    print('\n---------POPULATION DENSITY---------')
    data3 = {
        "India / State/ Union Territory": [
            "INDIA", "Andhra Pradesh", "Arunachal Pradesh", "Assam", "Bihar", "Chhattisgarh", "Goa", "Gujarat",
            "Haryana", "Himachal Pradesh", "Jammu & Kashmir", "Jharkhand", "Karnataka", "Kerala", "Madhya Pradesh",
            "Maharashtra", "Manipur", "Meghalaya", "Mizoram", "Nagaland", "Odisha", "Punjab", "Rajasthan",
            "Sikkim", "Tamil Nadu", "Telangana", "Tripura", "Uttarakhand", "Uttar Pradesh", "West Bengal",
            "Andaman & Nicobar Island", "Chandigarh", "Dadra & Nagar Haveli", "Daman & Diu", "Delhi",
            "Lakshadweep", "Puducherry"
        ],
        "Population Density (per sq.km) - 2011": [
            382, 308, 17, 398, 1106, 189, 394, 308, 573, 123, 124, 414, 319, 860, 236, 365, 115, 132, 52,
            119, 270, 551, 200, 86, 555, 307, 350, 189, 829, 1028, 46, 9258, 700, 2191, 11320, 2149, 2547
        ]
    }

    df3 = pd.DataFrame(data3)

    plt.figure(figsize=(12, 6))

    plt.plot(df3["India / State/ Union Territory"], df3["Population Density (per sq.km) - 2011"], marker='o', linestyle='-', color='blue')
    plt.xticks(rotation=90)
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Population Density (per sq.km) - 2011')
    plt.title('Population Density (per sq.km) - 2011 by State/Union Territory')
    plt.ylim(0, 12000)
    plt.grid(True)
    plt.tight_layout()

    plt.show()
    print('\n')
