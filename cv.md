# [rsschool-cv](https://alexamorw.github.io/)

# Alexandra Vodovozova

## Contacts
- phone +375 29 562-62-03
- email [morningstaralex013@gmail.com](mailto:morningstaralex013@gmail.com)
- website [alexamorw](https://alexamorw.github.io/)
- telegram [@alexandra_morningstar](t.me/alexandra_morningstart)
- GitHub [alexamorw]()

## About me
I have skills in the field of application development, website creation and website design. I also work in the field of computer design.

## Education
### Vitebsk State Technological University
Institution of higher education that teaches development skills.

## Skills

- C++
- Java
- Linux
- Krita
- Blender

## Code Example
```
#include <iostream>
#include <windows.h>
#include <math.h>

using namespace std;

class prm {
private:
    COORD p1, p2;

public:
    prm(int x1, int x2, int y1, int y2, bool t)
    {
        if (t) {
            p1.X = x1;
            p1.Y = y1;
            p2.X = x2;
            p2.Y = y2;
            cout << "A:" << "(" << x1 << "," << y1 << ")" << endl;
            cout << "B:" << "(" << x2 << "," << y1 << ")" << endl;
            cout << "C:" << "(" << x2 << "," << y2 << ")" << endl;
            cout << "D:" << "(" << x1 << "," << y2 << ")" << endl;
        }
        else {
            cout << "A:" << "(" << x1 << "," << y1 << ")" << endl;
            cout << "B:" << "(" << y1 + x1 << "," << y1 << ")" << endl;
            cout << "C:" << "(" << x1 + y1 << "," << y1 + y2 << ")" << endl;
            cout << "D:" << "(" << x1 << "," << y1 + y2 << ")" << endl;
        }

    }
   
    void perimeter()
    {
        cout << " Периметр прямоугольника:";
        cout << (2 * (p2.X - p1.X) + 2 * (p2.Y - p1.Y)) << endl;
    }
    void pl()
    {
        cout << " Площадь прямоугольника:";
        cout << ((p2.X - p1.X) * (p2.Y - p1.Y)) << endl;
    }
    void prover()
    {
        int x = 0; int y = 0;
        if ((p1.X < x < p2.Y) && (p1.Y < y < p2.Y))
        {
            cout << "да";
        }
        else {
            cout << "нeт";
        }
    }
};

int main()
{
    COORD p1, p2;
    int var, x, y, x1, x2, y1, y2, w, h;
    bool q;
    SetConsoleOutputCP(1251);
    cout << " выберите способ, чтобы задать прямоугольник: 1, 2 " << endl;
    cin >> var;
    if (var == 1)
    {
        q = true;
        cout << "Введите координаты x1, x2" << endl;
        cin >> p1.X >> p2.X;
        cout << "Введите координаты у1, у2" << endl;
        cin >> p1.Y >> p2.Y;
        cout << "Вы ввели следующие координаты прямоугольника:" << endl;
        prm z(p1.X, p1.Y, p2.X, p2.Y, q);
        z.perimeter();
        z.pl();
        cout << "Введите координаты точки, которую хотите проверить:" << endl;
        cin >> x >> y;
        z.prover();
    }
    else {
        q = false;
        cout << "Введите координаты x1, у1 одной точки" << endl;
        cin >> x1 >> y1;
        cout << "Введите длинну 1 стороны" << endl;
        cin >> w;
        cout << "введите длинну 2 стороны" << endl;
        cin >> h;
        x2 = x1 + w;
        y2 = y1 + h;
        cout << "x2=" << x1 + w << endl << "y2=" << y1 + h;
        prm m(x1, y1, w, h, q);
        m.perimeter();
        m.pl();
        cout << "Введите координаты точки, которую хотите проверить:" << endl;
        cin >> x >> y;
        m.prover();
    }
    system("pause");
    return 0;
}
```
