---
id: Practice
created_date: 2025-09-16
updated_date: 2025-09-16
type: practice
link: "[[University/OOP/Lecture 1|Lecture 1]]"
tags:
  - practice
  - 09-2025
  - IT
---

# Practice 1

### 1.
```C++
#include <iostream>
#include <windows.h>


int main()
{
    SetConsoleCP(1251);
    SetConsoleOutputCP(1251);

    std::string fir_name_1;
    std::string sec_name_1;
    std::string fir_name_2;
    std::string sec_name_2;
    std::string fir_name_3;
    std::string sec_name_3;
    int year_1;
    int year_2;
    int year_3;
    int month_1;
    int month_2;
    int month_3;

    std::cout << "Введите имя: ";
    std::cin >> fir_name_1;
    std::cout << "Введите фамилию: ";
    std::cin >> sec_name_1;
    std::cout << "Введите целое кол-во лет: ";
    std::cin >> year_1;
    std::cout << "Введите целое кол-во месяцев: ";
    std::cin >> month_1;
    std::cout << "Введите имя: ";
    std::cin >> fir_name_2;
    std::cout << "Введите фамилию: ";
    std::cin >> sec_name_2;
    std::cout << "Введите целое кол-во лет: ";
    std::cin >> year_2;
    std::cout << "Введите целое кол-во месяцев: ";
    std::cin >> month_2;
    std::cout << "Введите имя: ";
    std::cin >> fir_name_3;
    std::cout << "Введите фамилию: ";
    std::cin >> sec_name_3;
    std::cout << "Введите целое кол-во лет: ";
    std::cin >> year_3;
    std::cout << "Введите целое кол-во месяцев: ";
    std::cin >> month_3;

    int len_f1 = fir_name_1.length();
    int len_s1 = sec_name_1.length();

    int len_f2 = fir_name_2.length();
    int len_s2 = sec_name_2.length();

    int len_f3 = fir_name_3.length();
    int len_s3 = sec_name_3.length();


    int max_len_f = max(len_f1, len_f2, len_f3);
    int max_len_s = max(len_s1, len_s2, len_s3);

    while (fir_name_1.length() < max_len_f) {
        fir_name_1 = fir_name_1 + " ";
    }

    while (fir_name_2.length() < max_len_f) {
        fir_name_2 = fir_name_2 + " ";
    }

    while (fir_name_3.length() < max_len_f) {
        fir_name_3 = fir_name_3 + " ";
    }

    while (sec_name_1.length() < max_len_s) {
        sec_name_1 = sec_name_1 + " ";
    }
    while (sec_name_2.length() < max_len_s) {
        sec_name_2 = sec_name_2 + " ";
    }
    while (sec_name_3.length() < max_len_s) {
        sec_name_3 = sec_name_3 + " ";
    }

    int date_m_1 = year_1 * 12 + month_1;
    int date_d_1 = date_m_1 * 30;
    int date_m_2 = year_2 * 12 + month_2;
    int date_d_2 = date_m_2 * 30;
    int date_m_3 = year_3 * 12 + month_3;
    int date_d_3 = date_m_3 * 30;

    std::cout << "Имя: " << fir_name_1 << "\tФамилия: " << sec_name_1 << "\tКол-во месяцев: " << date_m_1 << "\tКол-во дней:" << date_d_3 << std::endl;
    std::cout << "Имя: " << fir_name_2 << "\tФамилия: " << sec_name_2 << "\tКол-во месяцев: " << date_m_2 << "\tКол-во дней:" << date_d_2 << std::endl;
    std::cout << "Имя: " << fir_name_3 << "\tФамилия: " << sec_name_3 << "\tКол-во месяцев: " << date_m_3 << "\tКол-во дней:" << date_d_1 << std::endl;


}
```


#### 2.
```C++
#include <iostream>


int main() {
	int n = 0;
	std::cout << n;
	int* pn = &n;
	*pn += 6;
	std::cout << *pn;
}
```

# Дз
