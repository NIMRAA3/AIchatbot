#include <iostream>
#include <string>
using namespace std;

// Function to generate chatbot responses
string getResponse(const string& input) {
    if (input == "hello" || input == "hi") {
        return "Hello! How can I assist you today?";
    } else if (input == "recommend me best books for IELTS preperation") {
        return "I recommended u to read vocabulary by paullline Cullen, barrons writing for IELTS !";
    } else if (input.find("thank") != string::npos) {
        return "You're welcome! Let me know if you need more help, best of luck! for your IELTS test.";
    } else {
        return "I'm sorry, I didn't understand that. Could you please rephrase?";
    }
}

int main() {
    string name, rollNo, userInput;

    // Ask for name and roll number
    cout << "Welcome to the AI Chatbot! Type 'exit' to end the conversation.\n";
    cout << "Enter your name: ";
    getline(cin, name);
    cout << "Enter your roll number: ";
    getline(cin, rollNo);

    cout << "\nHello " << name << " (Roll No: " << rollNo << ")! Let's start our conversation.\n";

    while (true) {
        cout << "\nYou: ";
        getline(cin, userInput);

        // Exit condition
        if (userInput == "exit") {
            cout << "Chatbot: Goodbye! Have a great day!\n";
            break;
        }

        // Call the function to get a response
        cout << "Chatbot: " << getResponse(userInput) << endl;
    }

    return 0;
}
