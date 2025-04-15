# Парсер биржевых данных с MFD.ru

## 📌 Описание
Автоматизированный парсер для сбора данных с сайта [mfd.ru](https://mfd.ru). Собирает актуальную информацию по:
- Котировкам акций
- Объемам торгов
- Изменениям цен
- Ключевым финансовым показателям

## 📊 Пример результатов

![Снимок данных за 2024-05-20](screenshots/sample_output.png)  
*Рис. 1: Данные по акциям (столбцы: тикер, цена, изменение в %)*

Или в текстовом формате:
```
Ticker^Time^Last Price^Change (abs)^Change (%)^Price before closing^Price at opening^Minimum price^Average overpriced^Pieces per day^Quantity per day^Rub^Number of transactions per day
+МосЭнерго^15:28:56^2.2015^-0.029^-1.30%^2.2305^2.2345^2.2^2.262^2.2295^16 291 000^36 324 747^2 883
2х Акции^15:28:09^955^+0.5^+0.05%^954.5^960^948.5^961.5^955^2 836^2 708 226^76
2хОФЗ^15:28:56^119 350^+1 250^+1.06%^118 100^120 300^119 000^120 300^120 150^116^13 939 400^9
AGROFRGT01^15:15:20^84.07^+1.98^+2.41%^82.09^81.66^81.66^84.9^83.93^396^332 377^80
AGRO-гдр^02.12.2024 23:50:01^1 083.8^-24^-2.17%^1 107.8^1 100.4^1 080^1 150.2^1 105.8^642 468^709 840 124^29 773
AKAI ETF^15:22:41^103.02^-1.27^-1.22%^104.29^104.29^102.97^104.29^103.77^560^58 111^96
AKBC ETF^15:26:26^96.4^+0.4^+0.42%^96^97.9^95.8^97.9^96.5^10 140^978 675^55
AKFB ETF^15:28:38^108.34^+0.23^+0.21%^108.11^108.11^107.93^108.5^108.27^480 742^52 048 958^431
AKGD ETF^15:28:52^195.84^-0.64^-0.33%^196.48^196.48^195.06^198.56^196.36^143 903^28 259 642^1 348
AKHT ETF^15:28:56^94.72^-0.2^-0.21%^94.92^94.92^94.41^95.66^95.18^7 053^671 318^203
```
## ⚙️ Технические характеристики
- **Язык программирования:** Python 3.11
- **Основные библиотеки:**
  - Selenium 4.9.1
  - Pandas 2.2.3
  - Fake-useragent 2.1.0
- **Режим работы:** headless (без графического интерфейса)
- **Формат данных:** CSV с разделителем "^"

## 🚀 Быстрый старт

### Установка
```bash
git clone https://github.com/yourrepo/mfd-parser.git
cd mfd-parser
python -m venv venv
source venv/bin/activate  # Для Windows: venv\Scripts\activate
pip install -r requirements.txt
