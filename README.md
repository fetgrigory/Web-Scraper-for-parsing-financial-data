# Парсер биржевых данных с MFD.ru

## 📌 Описание
Автоматизированный парсер для сбора данных с сайта [mfd.ru](https://mfd.ru/marketdata/?id=5&mode=0). Собирает актуальную информацию по:
- Котировкам акций
- Объемам торгов
- Изменениям цен
- Ключевым финансовым показателям

## 📊 Пример результатов
![Снимок экрана 2025-04-15 181313](https://github.com/user-attachments/assets/c56b828c-611a-4711-8c76-8b17dce7b690)
*Рис. 1: Данные по акциям*

### Структура данных
Поле | Описание
-----|---------
Ticker | Тикер ценной бумаги
Last Price | Последняя цена сделки
Change (abs)|  Абсолютное изменение цены
Change (%) | Изменение цены в процентах
Price before closing | Цена перед закрытием предыдущей сессии
Price at opening |  Цена при открытии текущей сессии
Minimum price |   Минимальная цена за сессию
Average overpriced |    Средняя цена
Pieces per day |    Количество лотов за день
Quantity per day | Общий объем сделок в штуках
Rub         | Объем сделок в рублях
Number of transactions per day | Количество сделок за день
## ⚙️ Технические характеристики
- **Язык программирования:** Python 3.11
- **Основные библиотеки:**
  - Selenium 4.31.0
  - webdriver-manager 4.0.2
  - Pandas 2.2.3
  - Fake-useragent 2.2.0
- **Режим работы:** headless (без графического интерфейса)
- **Формат данных:** CSV с разделителем "^"
## 🔍 Признаки MVP
### 1. Минимальная функциональность
- ✅ Парсинг только ключевых данных с одной страницы (`marketdata/?id=5&mode=0`)  
- ✅ Базовая обработка: очистка пустых строк, замена символов  
- ✅ Простое сохранение в CSV (без сложной ETL-цепочки)  
- ✅ Логирование основных событий  

### 2. Оптимальные технологии
- 🛠 **Selenium** - для работы с динамическим контентом  
- � **Pandas** - минимально необходимая обработка данных  
- 📝 **Логирование** - отслеживание ошибок через стандартный модуль  

### 3. Осознанные ограничения
- ⏳ Работа только в часы торгов (10:00-19:00 МСК, пн-пт)  
- 🔄 Интервал проверки - 10 минут (можно настроить)  
- 📂 Локальное хранение (без облаков и БД)  

## 🚀 Быстрый старт

### Установка
```bash
git clone https://github.com/fetgrigory/Web-Scraper-for-parsing-financial-data.git
cd mfd-parser
python -m venv venv
source venv/bin/activate  # Для Windows: venv\Scripts\activate
pip install -r requirements.txt
