# Інструкція з використання програми

### Опис програми TariffManager

Програма **TariffManager** призначена для управління тарифами мобільного зв'язку, аналізу даних про тарифи та клієнтів, а також виконання сортування і пошуку в заданих діапазонах цін.


### Основні можливості програми:
1. **Додавання тарифів**
   - Підтримка різних типів тарифів: базові, преміум і сімейні.

2. **Сортування тарифів**
   - За розміром абонентської плати.

3. **Пошук тарифів**
   - У визначеному ціновому діапазоні.

4. **Аналіз клієнтської бази**
   - Підрахунок загальної кількості клієнтів.

5. **Виведення результатів**
   - Демонстрація списку тарифів до та після обробки.


### Опис класів і методів

**1. Абстрактний клас `MobileTariff<T>`:**
- Представляє загальну структуру тарифу.
- **Методи:**
  - **Конструктор:** Ініціалізує основні параметри тарифу.
  - **getTotalCost():** Повертає загальну вартість послуг.
  - **compareTo():** Порівнює тарифи за щомісячною платою.
  - **toString():** Форматує дані тарифу для виводу.

**2. Клас `BasicTariff<T>`:**
- Реалізує базовий тариф з фіксованими параметрами.
- **getTotalCost():** Повертає місячну плату без додаткових послуг.

**3. Клас `PremiumTariff<T>`:**
- Реалізує преміум-тариф з можливістю включення роумінгу.
- **getTotalCost():** Включає додаткову плату за роумінг.

**4. Клас `FamilyTariff<T>`:**
- Реалізує сімейний тариф з кількома лініями.
- **getTotalCost():** Розраховує загальну вартість з урахуванням додаткових ліній.

**5. Клас `TariffManager`:**
- Управляє тарифами мобільного зв'язку.
- **Методи:**
  - **addTariff():** Додає новий тариф.
  - **getTotalClients():** Підраховує загальну кількість клієнтів.
  - **sortByMonthlyFee():** Сортує тарифи за абонентською платою.
  - **findTariffsByPriceRange():** Повертає список тарифів у заданому ціновому діапазоні.
  - **printTariffs():** Виводить список тарифів.


### Обробка помилок
- Перевірка правильності введених даних (негативні значення або некоректні діапазони).
- Генерація винятків з відповідними повідомленнями.


### Приклад роботи
**Список тарифів:**
```
Тариф 'Базовий' (ID: B1): 100.00 грн/міс, 1000 клієнтів
Тариф 'Преміум' (ID: P1): 500.00 грн/міс, 200 клієнтів
Тариф 'Сімейний' (ID: F1): 300.00 грн/міс, 150 клієнтів
```

**Загальна кількість клієнтів:**
```
1350
```

**Сортування тарифів за абонентською платою:**
```
Тариф 'Базовий' (ID: B1): 100.00 грн/міс, 1000 клієнтів
Тариф 'Сімейний' (ID: F1): 300.00 грн/міс, 150 клієнтів
Тариф 'Преміум' (ID: P1): 500.00 грн/міс, 200 клієнтів
```

**Пошук тарифів у діапазоні 200.00 - 400.00 грн:**
```
Тариф 'Сімейний' (ID: F1): 300.00 грн/міс, 150 клієнтів
```


**Запуск програми:**
   - Використайте термінал:
     ```bash
     javac TariffManager.java
     java TariffManager
     ```

## Результат виконання
Програма виведе:
- Список всіх тарифів
- Загальну кількість клієнтів
- Відсортований список тарифів за абонплатою
- Тарифи у заданому ціновому діапазоні

**Автор Демич Сергій**
