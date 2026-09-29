1. Месяцы 
#include <iostream>

enum Month 
{
    JANUARY = 1,
    FEBRUARY,
    MARCH,
    APRIL,
    MAY,
    JUNE,
    JULY,
    AUGUST,
    SEPTEMBER,
    OCTOBER,
    NOVEMBER,
    DECEMBER;
}

int main() 
{
    int input;

    while (true) 
    {
        std::cout << "Введите номер месяца (1–12) или 0 для выхода: " << std::endl;
        std::cin >> input;

        if (input == 0) 
        {
            std::cout << "Выход из программы." << std::endl;
            break;
        }

        if (input < 1 || input > 12) 
        {
            std::cout << "Некорректный номер месяца. Попробуйте снова." << std::endl;
            continue;
        }

        Month month = static_cast<Month>(input);

        switch (month) 
        {
            case JANUARY:   std::cout << "Январь"   << std::endl; break;
            case FEBRUARY:  std::cout << "Февраль"  << std::endl; break;
            case MARCH:     std::cout << "Март"     << std::endl; break;
            case APRIL:     std::cout << "Апрель"   << std::endl; break;
            case MAY:       std::cout << "Май"      << std::endl; break;
            case JUNE:      std::cout << "Июнь"     << std::endl; break;
            case JULY:      std::cout << "Июль"     << std::endl; break;
            case AUGUST:    std::cout << "Август"   << std::endl; break;
            case SEPTEMBER: std::cout << "Сентябрь" << std::endl; break;
            case OCTOBER:   std::cout << "Октябрь"  << std::endl; break;
            case NOVEMBER:  std::cout << "Ноябрь"   << std::endl; break;
            case DECEMBER:  std::cout << "Декабрь"  << std::endl; break;
        }
    }

    return 0;
}
