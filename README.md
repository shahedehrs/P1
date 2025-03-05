#include <iostream>
#include <vector>
#include <numeric>

using namespace std;

vector<int> get_ages(int count) {
    vector<int> ages;
    for (int i = 0; i < count; ++i) {
        int age;
        cout << "Enter age " << i + 1 << ": ";
        cin >> age;
        ages.push_back(age);
    }
    return ages;
}

int main() {
    vector<int> ages = get_ages(10);

    if (!ages.empty()) {
        double average = accumulate(ages.begin(), ages.end(), 0.0) / ages.size();
        cout << "Average age: " << average << endl;
    } else {
        cout << "No ages entered." << endl;
    }

    return 0;
}
