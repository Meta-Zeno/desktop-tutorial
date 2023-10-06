import random

print(""" _____                      _  _     __  __               _           
|_   _|__  __ _ _ __ ___   | || |   |  \/  |_   _ _ __ __| | ___ _ __ 
  | |/ _ \/ _` | '_ ` _ \  | || |_  | |\/| | | | | '__/ _` |/ _ \ '__|
  | |  __/ (_| | | | | | | |__   _| | |  | | |_| | | | (_| |  __/ |   
 _|_|\___|\__,_|_|_|_| |_|    |_|   |_|  |_|\__,_|_|  \__,_|\___|_|   
|  \/  |_   _ ___| |_ ___ _ __ _   _                                  
| |\/| | | | / __| __/ _ \ '__| | | |                                 
| |  | | |_| \__ \ ||  __/ |  | |_| |                                 
|_|  |_|\__, |___/\__\___|_|   \__, |                                 
        |___/                  |___/                                 
""")

def main():
    print("You are a CID officer in the UK Manchester. A murder call comes in.")
    
    while True:
        print("Do you want to accept the case? (yes/no)")
        response = input().lower()

        if response == "yes":
            crime_scene()
            break
        elif response == "no":
            print("You chose not to accept the case. You are a crap detective. You get fired and cannot find another job.")
            break
        else:
            print("Invalid choice. Please enter 'yes' or 'no'.")

def crime_scene():
    print("You have arrived at the crime scene. Start your investigation.")
    converse_with_officer()
    
    while True:
        print("Do you want to speak with the witnesses or go to the body on the floor? (witnesses/body)")
        response = input().lower()

        if response == "witnesses":
            print("You spoke with the witnesses. They have no further information to give.")
            search_body()
            break
        elif response == "body":
            search_body()
            break
        else:
            print("Invalid choice. Please enter 'witnesses' or 'body'.")

def converse_with_officer():
    print("You start speaking with the officer in charge.")
    print("They provide you with information about what witnesses have said.")
    # Here you can add more code for the conversation with the officer

def search_body():
    print("You search the body. You find multiple stab wounds and a note with a name and a time. You keep the note for later.")
    search_area()
    # Here you can add more code for searching the body

def search_area():
    print("You proceed to search the area around the crime scene and find some potential places to hide the murder weapon.")
    weapon_search()

def weapon_search():
    while True:
        print("Do you want to search the bins, carboard boxes or the gutter")
        response = input().lower()

        if response == "bins":
            print("You search the surrounding area in various bins and find nothing.")
            search_bin()
            break
        elif response == "cardboard boxes":
            print("You search the surrounding area in various bins and find nothing.")
            search_cardboard_box()
            break
        elif response == "gutter":
            search_gutter()
            break
        else:
            print("Invalid choice. Please enter 'bins, cardboard box or gutter`.")

def search_bin():
    print("You do not find anything useful")  
    weapon_search() 

def search_cardboard_box():
    print("You find nothing in the boxes of use")
    weapon_search()

def search_gutter():
    print("You find a knife covered in blood.")
    print(""" 
       .---.
       |---|
       |---|
       |---|
   .---^ - ^---.
   :___________:
      |  |//|
      |  |//|
      |  |//|
      |  |//|
      |  |//|
      |  |//|
      |  |.-|
      |.-'**|
       \***/
        \*/
         V

        '
         ^'
        (_)

    -.   ^   .-
______\'.|.'/________                      
""")
    print("You decide to leave the scene and go back to the lab.")
    go_to_lab()



def go_to_lab():
    print("You arrive at the lab with the blood stained knife and run some DNA tests.")
    dna_randomiser()

def dna_randomiser():
    print("You place some collected blood from the knife and test the dna against known suspects in the police database.")
    match_probability = random.random()  # Generate a random number between 0 and 1
    
    def dna_positive():
        print("A warrent is made for the arrest of the suspect called Bob. They are brought before the court and charged with murder of the victim. They are senteced to 10 years in prison")
        bob_jailed()
        
    def bob_jailed():
        print("Bob is not happy that he was jailed by you. He wishes that you were the victim. He also has a death wish on you and people will eventually catch up with you and kill you.")
        print("""
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣴⠏⠁⠀⠙⢿⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⣿⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⡏⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣿⡇⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣿⡇⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣿⡇⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣠⣶⠶⣶⣿⠀⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣾⠏⠀⠀⠈⣿⠀⠀⠀⠀⠀⢸⣷⣦⣤⣄⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣼⡿⠀⠀⠀⠀⣿⠀⠀⠀⠀⠀⢸⠇⠀⠀⠉⢷⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣠⡾⢿⠇⠀⠀⠀⠀⣿⠀⠀⠀⠀⠀⢸⡇⠀⠀⠀⠸⡷⠤⣄⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⡾⠋⠀⣾⠀⠀⠀⠀⠀⣿⠀⠀⠀⠀⠀⢸⡇⠀⠀⠀⠀⣧⠀⠀⠹⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣰⠏⠀⠀⠀⣿⠀⠀⠀⠀⠀⠉⠀⠀⠀⠀⠀⠈⠁⠀⠀⠀⠀⢹⡄⠀⠀⢹⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⢰⡏⠀⠀⠀⠀⡏⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠘⠇⠀⠀⠀⢻⡄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠘⣿⡀⠀⠀⠀⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠸⣷⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠙⢿⣦⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⣿⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠹⣷⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣼⡟⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠻⣷⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣼⠟⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠻⣧⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣴⡿⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⢿⣦⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣼⠏⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⡏⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⡏⠀⠀⠀⠀⠀⠀⠀⠀
        
        
 _____ _     _       _                _           _     ____        _     
|_   _| |__ (_)___  (_)___  __      _| |__   __ _| |_  | __ )  ___ | |__  
  | | | '_ \| / __| | / __| \ \ /\ / / '_ \ / _` | __| |  _ \ / _ \| '_ \ 
  | | | | | | \__ \ | \__ \  \ V  V /| | | | (_| | |_  | |_) | (_) | |_) |
 _|_|_|_| |_|_|___/_|_|___/   \_/\_/ |_| |_|\__,_|\__| |____/ \___/|_.__/ 
| |_| |__ (_)_ __ | | _____    ___  / _|  _   _  ___  _   _               
| __| '_ \| | '_ \| |/ / __|  / _ \| |_  | | | |/ _ \| | | |              
| |_| | | | | | | |   <\__ \ | (_) |  _| | |_| | (_) | |_| |_             
 \__|_| |_|_|_| |_|_|\_\___/  \___/|_|    \__, |\___/ \__,_(_)            
                                          |___/                           
""")
        
    def dna_negative():
        print("Due to the dna coming back negative your only supect walks free!")
        failed_game_over()

    if match_probability < 0.5:  # Set the match probability to 50%
        print("The DNA matches a criminal in the database.")
        dna_positive()
    else:
        print("The DNA does not match any criminal in the database.")
        dna_negative()

def failed_game_over():
    print("The game is over, you failed this case and the victim.")
    print("""
    
   ⢀⣤⣶⣶⣤⣄⡀
⠀⢀⣿⣿⣿⣿⣿⣿⣿⡆
⠀⠸⣿⣿⣿⣿⣿⡟⡟⡗ ⣿⠉⣿⠉⣿⡏⠹⡏⢹⡏⢹⣿⣿⠉⣿⠉⣿⡟⢋⠛⣿⠉⡟⢉⡏⠹⠏⣹⣿
⠀⠀⠙⠏⠯⠛⣉⢲⣧⠟ ⣿⠄⣿⠄⣿⡇⡄⠁⢸⡇⢸⣿⣿⠄⣿⠄⣿⠄⣿⣿⣿⠄⡀⢻⣿⡄⢠⣿⣿
⠀⠀⠠⢭⣝⣾⠿⣴⣿⠇ ⣿⣦⣤⣴⣿⣧⣿⣤⣼⣧⣬⣭⣿⣦⣤⣴⣿⣧⣤⣤⣿⣤⣷⣤⣿⣧⣼⣿⣿
⠀⠀⢐⣺⡿⠁⠀⠈⠉⠀⠀⠀⠀⠀⠀⠀⠀⠀ ⣶⣶⣶⣶⣶⣶⠀
⠀⠀⣚⣿⠃ ⣶⣶⣶⣶
⢀⣿⣿⣿⣷⢒⣢⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣠⣶⣶⣄⠄
⢰⣿⣿⡿⣿⣦⠬⢝⡄⠀⠀⠀⠀⠀⠀⢠⣿⠿⠿⠟⠛⠋⠁
⠠⢿⣿⣷⠺⣿⣗⠒⠜⡄⠀⠀⠀⠀⣴⠟⠁
⠀⣰⣿⣷⣍⡛⣯⣯⣙⡁⠀⠀⣠⡾⠁
⠀⠨⢽⣿⣷⢍⣛⣶⢷⣼⣠⣾⠋
⠀⠀⠘⢿⣿⣖⠬⣹⣶⣿⠟⠁
⠀⠀⠀⠚⠿⠿⡒⠨⠛⠋
⠀⠀⠀⠐⢒⣛⣷
⠀⠀⠀⢘⣻⣭⣭
⠀⠀⠀⡰⢚⣺⣿
⠀⠀⢠⣿⣿⣿⣿⣦⡄
⠀⠀⢸⡿⢿⣿⢿⡿⠃
⠀⠀⠘⡇⣸⣿⣿⣿⣆
⠀⠀⠀⠀⠸⣿⡿⠉⠁
⠀⠀⠀⠀⠀⢿⡟
    
⢿⣿⣿⣿⣭⠹⠛⠛⠛⢿⣿⣿⣿⣿⡿⣿⠷⠶⠿⢻⣿⣛⣦⣙⠻⣿
⣿⣿⢿⣿⠏⠀⠀⡀⠀⠈⣿⢛⣽⣜⠯⣽⠀⠀⠀⠀⠙⢿⣷⣻⡀⢿
⠐⠛⢿⣾⣖⣤⡀⠀⢀⡰⠿⢷⣶⣿⡇⠻⣖⣒⣒⣶⣿⣿⡟⢙⣶⣮
⣤⠀⠀⠛⠻⠗⠿⠿⣯⡆⣿⣛⣿⡿⠿⠮⡶⠼⠟⠙⠊⠁⠀⠸⢣⣿
⣿⣷⡀⠀⠀⠀⠀⠠⠭⣍⡉⢩⣥⡤⠥⣤⡶⣒⠀⠀⠀⠀⠀⢰⣿⣿
⣿⣿⡽⡄⠀⠀⠀⢿⣿⣆⣿⣧⢡⣾⣿⡇⣾⣿⡇⠀⠀⠀⠀⣿⡇⠃
⣿⣿⣷⣻⣆⢄⠀⠈⠉⠉⠛⠛⠘⠛⠛⠛⠙⠛⠁⠀⠀⠀⠀⣿⡇⢸
⢞⣿⣿⣷⣝⣷⣝⠦⡀⠀⠀⠀⠀⠀⠀⠀⡀⢀⠀⠀⠀⠀⠀⠛⣿⠈
⣦⡑⠛⣟⢿⡿⣿⣷⣝⢧⡀⠀⠀⣶⣸⡇⣿⢸⣧⠀⠀⠀⠀⢸⡿⡆
⣿⣿⣷⣮⣭⣍⡛⠻⢿⣷⠿⣶⣶⣬⣬⣁⣉⣀⣀⣁⡤⢴⣺⣾⣽⡇

    """)
    quit()
    
        
if __name__ == "__main__":
        main()

