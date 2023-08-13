#include <iostream>
#include <string>

int main() {
    std::cout << "Welcome to the Text Adventure Game!\n";
    
    std::string playerName;
    std::cout << "Enter your name: ";
    std::cin >> playerName;
    
    std::cout << "Hello, " << playerName << "! You find yourself in a dark forest.\n";
    std::cout << "You have two paths ahead of you. Will you go left or right?\n";
    
    std::string pathChoice;
    std::cin >> pathChoice;
    
    if (pathChoice == "left") {
        std::cout << "You encounter a river. Do you swim across or find a bridge?\n";
        std::cin >> pathChoice;
        
        if (pathChoice == "swim") {
            std::cout << "You try to swim across, but the current is too strong...\n";
            std::cout << "Unfortunately, your adventure ends here. Game over!\n";
        } else if (pathChoice == "bridge") {
            std::cout << "You find a sturdy bridge and cross safely.\n";
            std::cout << "Ahead, you see a treasure chest. Do you open it?\n";
            std::cin >> pathChoice;
            
            if (pathChoice == "yes") {
                std::cout << "Congratulations, " << playerName << "! You found the hidden treasure.\n";
                std::cout << "You are victorious!\n";
            } else {
                std::cout << "You decide to leave the chest alone and continue your journey.\n";
                std::cout << "You successfully navigate the forest and reach the end of your adventure.\n";
            }
        }
    } else if (pathChoice == "right") {
        std::cout << "You come across a pack of wolves. Will you fight or run?\n";
        std::cin >> pathChoice;
        
        if (pathChoice == "fight") {
            std::cout << "You bravely fight off the wolves, but you are injured in the process...\n";
            std::cout << "You manage to escape and find shelter. Your adventure continues.\n";
        } else if (pathChoice == "run") {
            std::cout << "You run away from the wolves, but they catch up to you...\n";
            std::cout << "Unfortunately, your adventure ends here. Game over!\n";
        }
    } else {
        std::cout << "You can't decide and stand still. Time passes...\n";
        std::cout << "You are overtaken by darkness. Your adventure ends here. Game over!\n";
    }
    
    return 0;
}
