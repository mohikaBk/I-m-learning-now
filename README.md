#include <iostream>
using namespace std;

const int MAX = 50;

int main() {
    int n, mt[MAX + 1][MAX + 1];
    cin >> n;
    for (int i = 1; i <= n; ++i) {
        for (int j = 1; j <= n; ++j) {
            cin >> mt[i][j];
        }
    }
    for (int i = 1; i <= n; ++i) {
        for (int j = 1; j <= n; ++j) {
            cout << mt[i][j] << " ";
        }
        cout << "\n";
    }
    for (int i = 1; i <= n; ++i) {
        for (int j = 1; j <= n; ++j) {
            if (i == j || j == n - i + 1) {
                cout << mt[i][j] << " ";  
            } else {
                cout << mt[i + j == n - 1][i] << " "; 
            }
        }
        cout << "\n";
    }
    return 0;
}
