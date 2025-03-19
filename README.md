
# C-_Activity1
#include <iostream>
#include <string>
using namespace std;

class TrafficSignal {
private:
    int signal_Id;
    string state;

public:
    TrafficSignal(int id, string initialState) {
        signal_Id = id;
        state = initialState;
    }

    void changeState(string newState) {
        state = newState;
    }

    void display() {
        cout << "Signal ID: " << signal_Id << " - State: " << state << endl;
    }
};

int main() {
    TrafficSignal signals[3] = {
        TrafficSignal(1, "Red"),
        TrafficSignal(2, "Yellow"),
        TrafficSignal(3, "Green")
    };

    cout << "Initial Signal States:\n";
    for (int i = 0; i < 3; i++) {
        signals[i].display();
    }

    signals[0].changeState("Green");
    signals[1].changeState("Red");
    signals[2].changeState("Yellow");

    cout << "\nUpdated Signal States:\n";
    for (int i = 0; i < 3; i++) {
        signals[i].display();
    }

    return 0;
}