import random

class Player:
    def __init__(self, name, wealth):
        self.name = name
        self.wealth = wealth
        self.location = "Player's Mansion"  # Starting location
        self.inventory = []
        self.cars = ["Ferrari", "Lamborghini", "Tesla", "BMW", "Mercedes"]  # List of cars available to the player
        self.has_phone = True

    def move(self, destination):
        self.location = destination

    def work(self):
        # Implement player's ability to work and earn money
        pass

class Game:
    def __init__(self):
        self.players = []

    def add_player(self, player):
        self.players.append(player)

    def display_main_menu(self):
        print("Welcome to Open World Game")
        print("1. Start Game")
        print("2. Settings")
        print("3. Quit")

    def display_settings_menu(self):
        print("Settings Menu")
        print("1. Graphic Settings")
        print("2. UI Settings")
        print("3. Back to Main Menu")

    def play(self):
        # Initialize game
        player = Player("Player", 1000000)  # Player starts with 1,000,000 wealth
        self.add_player(player)

        # Main game loop
        while True:
            self.display_main_menu()
            choice = input("Enter your choice: ")

            if choice == '1':
                self.start_game(player)
            elif choice == '2':
                self.display_settings_menu()
                settings_choice = input("Enter your choice: ")
                if settings_choice == '1':
                    self.adjust_graphics()
                elif settings_choice == '2':
                    self.adjust_ui()
                elif settings_choice == '3':
                    pass  # Back to Main Menu
                else:
                    print("Invalid choice. Please try again.")
            elif choice == '3':
                print("Exiting game. Goodbye!")
                break
            else:
                print("Invalid choice. Please try again.")

    def start_game(self, player):
        print(f"Welcome, {player.name}!")
        print("You are starting the game from your mansion.")
        print("You have access to various cars and a phone.")
        print("Enjoy your adventure in the open world of Dubai!")

    def adjust_graphics(self):
        print("Adjusting graphic settings...")
        # Implement graphic settings functionality

    def adjust_ui(self):
        print("Adjusting UI settings...")
        # Implement UI settings functionality

if __name__ == "__main__":
    game = Game()
    game.play()
