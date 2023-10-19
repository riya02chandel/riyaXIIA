import pandas as pd
import matplotlib.pyplot as plt

print(":)")
print("#1. For checking the data.")
print("===================")
print("Topic - Population of India(2011)")
print(" ")
print("    Press 1 to create a line chart for total population")
print("    Press 2 to create a line chart for decadal population growth rate.")
print("    Press 3 to create a line chart for population density.")
print(" ")
print("    Press 4 to create a bar graph for total population.")
print("    Press 5 to create a bar graph for decadal population growth rate.")
print("    Press 6 to create a bar graph for population density.")
print(" ")
print("#7. For Exit")
print("===============")

choice2 = int(input('Enter your choice: '))

a = pd.read_csv("C:/Users/riyac/PycharmProjects/pythonProject/total population.csv")

if choice2 == 1:
    print('\n---------TOTAL POPULATION---------')
    df1 = pd.DataFrame(a)
    
    plt.figure(figsize=(12, 6))
    plt.plot(df1["India / State/ Union Territory"], df1["Population - 2011"], marker='o', linestyle='-', color='red')
    plt.title('Population - 2011 by India / State/ Union Territory')
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Population - 2011')
    plt.xticks(rotation=90)
    plt.grid(True)
    plt.tight_layout()
    
    plt.show()
    print('\n')

elif choice2 == 2:
    print('\n---------DECADEL POPULATION GROWTH RATE---------')
    df2 = pd.DataFrame(a)
    
    plt.figure(figsize=(12, 6))
    
    plt.plot(df2["India / State/ Union Territory"], df2["Decadal Population Growth Rate "], marker='o', linestyle='-', 
             color='blue')
    plt.xticks(rotation=90)
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Decadal Population Growth Rate ')
    plt.title('Decadal Population Growth Rate  by State/Union Territory')
    plt.grid(True)
    plt.tight_layout()
    
    plt.show()
    print('\n')

elif choice2 == 3:
    print('\n---------POPULATION DENSITY---------')
    df3 = pd.DataFrame(a)
    
    plt.figure(figsize=(12, 6))
    
    plt.plot(df3["India / State/ Union Territory"], df3["Population Density (per sq.km) - 2011"], marker='o', linestyle='-',
             color='orange')
    plt.xticks(rotation=90)
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Population Density (per sq.km) - 2011')
    plt.title('Population Density (per sq.km) - 2011 by State/Union Territory')
    plt.ylim(0, 12000)
    plt.grid(True)
    plt.tight_layout()
    
    plt.show()
    print('\n')

elif choice2 == 4:
    print('\n---------TOTAL POPULATION---------')
    df4 = pd.DataFrame(a)
    
    plt.figure(figsize=(12, 10))
    plt.bar(df4["India / State/ Union Territory"], df4["Population - 2011"], color='green')
    plt.title('Population - 2011 by India / State/ Union Territory')
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Population - 2011')
    plt.xticks(rotation=90)
    plt.tight_layout()
    
    plt.show()
    print('\n')
    
    
    
elif choice2 == 5:
    df5 = pd.DataFrame(a)

    plt.figure(figsize=(12, 6))
    plt.bar(df5["India / State/ Union Territory"], df5["Decadal Population Growth Rate "], color='black')
    plt.xticks(rotation=90)
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Decadal Population Growth Rate ')
    plt.title('Decadal Population Growth Rate by State/Union Territory')
    plt.tight_layout()

    plt.show()
    print('\n')
    
elif choice2 == 6:
    df3 = pd.DataFrame(a)

    plt.figure(figsize=(12, 6))
    plt.bar(df3["India / State/ Union Territory"], df3["Population Density (per sq.km) - 2011"], color='pink')
    plt.xticks(rotation=90)
    plt.xlabel('India / State/ Union Territory')
    plt.ylabel('Population Density (per sq.km) - 2011')
    plt.title('Population Density (per sq.km) - 2011 by State/Union Territory')
    plt.tight_layout()

    plt.show()
    print('\n')

else:       
    print("thank you")

    
    
    
    
    

    
