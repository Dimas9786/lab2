# lab2
laba z op
include <iostream>
#include <cmath>

using namespace std;

// Функція для обчислення значення F
double calculateF(double a, double b, double c, double x) {
    int A = static_cast<int>(a);
    int B = static_cast<int>(b);
    int C = static_cast<int>(c);

    if (((A * C) | B) % 2 != 0) {
        if (x - 1 < 0 && b - x != 0)
            return a * pow(x, 2) + b;
        else if (x - 1 > 0 && b + x == 0)
            return x - a;
    }

    return 6.0;
}

int main() {
    double a, b, c, X_start, X_end, H;

    // Зчитуємо значення з клавіатури
    cout << "Введіть значення a: ";
    cin >> a;
    cout << "Введіть значення b: ";
    cin >> b;
    cout << "Введіть значення c: ";
    cin >> c;
    cout << "Введіть початкове значення X: ";
    cin >> X_start;
    cout << "Введіть кінцеве значення X: ";
    cin >> X_end;
    cout << "Введіть крок H: ";
    cin >> H;

    // Виводимо заголовок таблиці
    cout << "X\tF(X)" << endl;

    // Обчислюємо та виводимо значення F на заданому інтервалі
    for (double x = X_start; x <= X_end; x += H) {
        double result = calculateF(a, b, c, x);
        cout << x << "\t" << result << endl;
    }

    return 0;
}
