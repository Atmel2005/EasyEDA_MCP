# 🚀 EasyEDA Pro AI Automation Plugin & MCP Server

https://github.com/Atmel2005/EasyEDA_MCP/raw/main/install.mp4

<!-- markdownlint-disable MD024 -->

## Deutsch

Schöpfen Sie das verborgene Potenzial von EasyEDA Pro aus! Dieses Plugin und der MCP-Server (Model Context Protocol) verwandeln Ihre Lieblings-KI (Claude, Antigravity, ChatGPT) in einen erfahrenen PCB-Designer. Vergessen Sie endloses manuelles Klicken – bitten Sie die KI einfach, Ihre Leiterplatte zu routen, Komponenten auszurichten oder 3D-Modelle zuzuweisen.

Durch die Injektion einer WebSocket-Bridge direkt in die CAD-Umgebung öffnet dieses Tool der KI ein riesiges Arsenal von **über 670 undokumentierten internen API-Befehlen**.

### ✨ Magische Funktionen

Das Plugin bietet vollständigen "God-Mode"-Zugriff auf die gesamte interne API von EasyEDA Pro. Hier ist eine kurze Liste der programmgesteuerten Funktionen:

- **Projekt- & Dateiverwaltung:** Projekte, Schaltpläne und Leiterplatten erstellen, öffnen und umbenennen. Die gesamte Struktur des aktuellen Projekts auslesen.
- **Schaltplan-Operationen (SCH):** Alles auslesen: Komponenten, Netzlisten (Netlists), Verbindungen (Wires) und Pins. Komponenten im Schaltplan erstellen, löschen und verschieben. Drahtverbindungen programmatisch zeichnen. Beliebige Elementeigenschaften (Werte, Bezeichner, Attribute) ändern.
- **PCB-Operationen:**
  - **Platzierung (Placement):** Koordinaten beliebiger Elemente auslesen und diese nach benutzerdefinierten Regeln verschieben/drehen.
  - **Routing:** Leiterbahnen (Tracks) beliebiger Breite auf jeder Ebene zeichnen, Vias erstellen und Kupferflächen (Pours) gießen.
  - **Board-Management:** Den Platinenumriss (Board Outline), die Ebenen bearbeiten und DRC-Regeln auslesen.
- **Vollständige Anpassung:** Das Plugin kann on-the-fly JavaScript-Makros direkt in der EasyEDA-Umgebung generieren und ausführen, um jede Routineaufgabe zu automatisieren, die mit der Maus erledigt werden kann.

**Kurz gesagt:** Alles, was die EasyEDA-API erlaubt, kann dieses Plugin auf Ihre Anfrage hin autonom ausführen.

### 🛠️ Installation (Antigravity / Claude Desktop ↔ EasyEDA Pro)

- Laden Sie die Datei `easyeda_plugin.eext` (oder `.zip`) über den Extension Manager in EasyEDA Pro.
- Fügen Sie die MCP-Server-Konfiguration zu Ihrem KI-Client (z. B. Antigravity oder Claude Desktop) hinzu:

```json
"easyeda_pro": {
  "command": "python",
  "args": [
    "C:/path/to/your/EasyEDA_MCP/easyeda_mcp.py"
  ]
}
```

### 🔌 Verbindung

- MCP Server Port: `stdio`
- WebSocket Bridge Port: `8787`
- Ziel-URL: `https://pro.easyeda.com/editor`

### 🎮 Nutzung

1. Den MCP-Server über die Konfiguration des KI-Clients starten.
2. EasyEDA Pro im Browser öffnen; das Plugin verbindet sich automatisch über WebSocket.
3. Die KI bitten: "Platziere alle Komponenten auf der Leiterplatte" oder "Weise meinen Widerständen 3D-Modelle zu".
4. Die KI liest den API-Katalog und führt die Magie live in Ihrem Editor aus!

**Serielle Ausgabe (Beispiel):**

```text
[INFO] Starting EasyEDA WebSocket Server on ws://localhost:8787
[INFO] ATM_MCP WebSocket connected
[INFO] ATM_MCP event: execute-js
```

### 📦 Build/Run

- Python 3.10+
- `websockets` Bibliothek
- Chrome/Edge Browser

### ⚠️ Hinweise

- Stellen Sie sicher, dass EasyEDA Pro geöffnet und der aktive Tab ist, bevor komplexe PCB-Platzierungsmakros ausgeführt werden.
- Da die KI Zugriff auf die vollständige undokumentierte API hat, können komplexe Makros je nach EasyEDA-Version Versuch und Irrtum erfordern.

---

## Українська

Повністю розкрийте прихований потенціал EasyEDA Pro! Цей плагін та MCP (Model Context Protocol) сервер перетворюють ваш улюблений ШІ (Claude, Antigravity, ChatGPT) на експерта з проєктування друкованих плат. Забудьте про нескінченне ручне клікання — просто попросіть ШІ розвести плату, вирівняти компоненти або призначити 3D-моделі.

Впроваджуючи WebSocket-міст безпосередньо в середовище CAD, цей інструмент відкриває для ШІ величезний арсенал з **понад 670 прихованих внутрішніх API-команд**.

### ✨ Магічні можливості

Плагін надає повний "God-mode" доступ до всього внутрішнього API EasyEDA Pro. Ось короткий список того, що плагін вміє робити програмно:

- **Управління проєктами та файлами:** Створювати, відкривати та перейменовувати проєкти, схеми та друковані плати. Зчитувати всю структуру поточного проєкту.
- **Робота зі схемами (SCH):** Зчитувати абсолютно все: список компонентів, ланцюгів (Netlist), з'єднань (Wires), виводів (Pins). Створювати, видаляти та переміщати компоненти на схемі. Програмно малювати лінії з'єднань між виводами. Змінювати будь-які властивості елементів (номінали, позиційні позначення, атрибути).
- **Робота з друкованими платами (PCB):**
  - **Розміщення (Placement):** Зчитувати координати будь-яких елементів і переміщати/обертати їх за потрібними правилами.
  - **Трасування (Routing):** Малювати доріжки (Tracks) потрібної ширини на будь-якому шарі, створювати перехідні отвори (Vias) та мідні полігони (Pours).
  - **Управління платою:** Редагувати контур плати (Board Outline), шари та зчитувати правила DRC.
- **Повна кастомізація:** Плагін може на льоту генерувати та виконувати будь-який JavaScript-макрос прямо в середовищі EasyEDA, автоматизуючи будь-яку рутину, яку можна зробити мишкою.

**Коротше кажучи:** все, що дозволяє робити API EasyEDA, цей плагін може робити автономно за вашим запитом.

### 🛠️ Встановлення (Antigravity / Claude Desktop ↔ EasyEDA Pro)

- Завантажте файл `easyeda_plugin.eext` (або `.zip`) через менеджер розширень в EasyEDA Pro.
- Додайте конфігурацію MCP-сервера до вашого клієнта ШІ (наприклад, Antigravity або Claude Desktop):

```json
"easyeda_pro": {
  "command": "python",
  "args": [
    "C:/path/to/your/EasyEDA_MCP/easyeda_mcp.py"
  ]
}
```

### 🔌 З'єднання

- MCP Server Port: `stdio`
- WebSocket Bridge Port: `8787`
- Цільова URL: `https://pro.easyeda.com/editor`

### 🎮 Як користуватися

1. Запустити MCP-сервер через конфігурацію клієнта ШІ.
2. Відкрити EasyEDA Pro у браузері; плагін автоматично підключиться через WebSocket.
3. Попросити ШІ "Розмістити всі компоненти на платі" або "Призначити 3D-моделі моїм резисторам".
4. ШІ прочитає каталог API та виконає магію в реальному часі у вашому редакторі!

**Приклад виводу в консоль:**

```text
[INFO] Starting EasyEDA WebSocket Server on ws://localhost:8787
[INFO] ATM_MCP WebSocket connected
[INFO] ATM_MCP event: execute-js
```

### 📦 Збірка/Запуск

- Python 3.10+
- Бібліотека `websockets`
- Браузер Chrome/Edge

### ⚠️ Примітки

- Переконайтеся, що EasyEDA Pro відкрито і це активна вкладка перед запуском складних макросів для розміщення на PCB.
- Оскільки ШІ має доступ до повного недокументованого API, складні макроси можуть вимагати методу спроб і помилок залежно від версії EasyEDA.

---

## English

Unlock the hidden potential of EasyEDA Pro! This plugin and MCP (Model Context Protocol) server turn your favorite AI (Claude, Antigravity, ChatGPT) into an expert PCB designer. Forget about endless manual clicking—simply ask the AI to route your board, align components, or assign 3D models.

By injecting a WebSocket bridge directly into the CAD environment, this tool exposes a massive arsenal of **over 670 undocumented internal API commands** to the AI.

### ✨ Magical Features

The plugin provides full "God-mode" access to the entire internal API of EasyEDA Pro. Here is a brief list of what the plugin can do programmatically:

- **Project & File Management:** Create, open, and rename projects, schematics, and PCBs. Read the entire structure of the current project.
- **Schematic (SCH) Operations:** Read absolutely everything: components, netlists, wires, and pins. Create, delete, and move schematic components. Programmatically draw wire connections. Modify any element properties (values, designators, attributes).
- **PCB Operations:**
  - **Placement:** Read coordinates of any elements and move/rotate them according to custom rules.
  - **Routing:** Draw tracks of any width on any layer, create vias, and pour copper.
  - **Board Management:** Edit the board outline, layers, and read DRC rules.
- **Full Customization:** The plugin can generate and execute any JavaScript macro on the fly directly inside the EasyEDA environment, automating any routine task that can be done with a mouse.

**In short:** anything the EasyEDA API allows, this plugin can do autonomously upon your request.

### 🛠️ Installation (Antigravity / Claude Desktop ↔ EasyEDA Pro)

- Load the `easyeda_plugin.eext` (or `.zip`) file via the Extension Manager in EasyEDA Pro.
- Add the MCP server configuration to your AI client (e.g. Antigravity or Claude Desktop):

```json
"easyeda_pro": {
  "command": "python",
  "args": [
    "C:/path/to/your/EasyEDA_MCP/easyeda_mcp.py"
  ]
}
```

### 🔌 Connection

- MCP Server Port: `stdio`
- WebSocket Bridge Port: `8787`
- Target URL: `https://pro.easyeda.com/editor`

### 🎮 How to use

1. Start the MCP server via your AI client's configuration.
2. Open EasyEDA Pro in the browser; the plugin will automatically connect via WebSocket.
3. Ask the AI to "Place all components on the PCB" or "Assign 3D models to my resistors".
4. The AI will read the API catalog and execute the magic live in your editor!

**Server output (example):**

```text
[INFO] Starting EasyEDA WebSocket Server on ws://localhost:8787
[INFO] ATM_MCP WebSocket connected
[INFO] ATM_MCP event: execute-js
```

### 📦 Build/Run

- Python 3.10+
- `websockets` library
- Chrome/Edge browser

### ⚠️ Notes

- Ensure EasyEDA Pro is open and the active tab before running complex PCB placement macros.
- Because the AI has access to the full undocumented API, complex macros might require some trial and error depending on the EasyEDA version.

---

## Русский

Полностью раскройте скрытый потенциал EasyEDA Pro! Этот плагин и MCP (Model Context Protocol) сервер превращают ваш любимый ИИ (Claude, Antigravity, ChatGPT) в эксперта по проектированию печатных плат. Забудьте про бесконечное ручное кликание — просто попросите ИИ развести плату, выровнять компоненты или назначить 3D-модели.

Внедряя WebSocket-мост напрямую в среду CAD, этот инструмент открывает для ИИ огромный арсенал из **более чем 670 скрытых внутренних API-команд**.

### ✨ Магические возможности

Плагин предоставляет полный "God-mode" доступ ко всему внутреннему API EasyEDA Pro. Вот краткий список того, что плагин умеет делать программно:

- **Управление проектами и файлами:** Создавать, открывать и переименовывать проекты, схемы и печатные платы. Считывать всю структуру текущего проекта.
- **Работа со схемами (SCH):** Считывать абсолютно всё: список компонентов, цепей (Netlist), соединений (Wires), выводов (Pins). Создавать, удалять и перемещать компоненты на схеме. Программно рисовать линии соединений между выводами. Изменять любые свойства элементов (номиналы, позиционные обозначения, атрибуты).
- **Работа с печатными платами (PCB):**
  - **Расстановка (Placement):** Считывать координаты любых элементов и перемещать/поворачивать их по нужным правилам.
  - **Трассировка (Routing):** Рисовать дорожки (Tracks) нужной ширины на любом слое, создавать переходные отверстия (Vias) и медные полигоны (Pours).
  - **Управление платой:** Редактировать контур платы (Board Outline), слои и считывать правила DRC.
- **Полная кастомизация:** Плагин может на лету генерировать и выполнять любой макрос или JavaScript-код прямо внутри среды EasyEDA, автоматизируя любую рутину, которую можно сделать мышкой.

**Короче говоря:** всё, что позволяет делать API EasyEDA, этот плагин может делать автономно по вашему запросу.

### 🛠️ Установка (Antigravity / Claude Desktop ↔ EasyEDA Pro)

- Загрузите файл `easyeda_plugin.eext` (или `.zip`) через менеджер расширений в EasyEDA Pro.
- Добавьте конфигурацию MCP-сервера в ваш ИИ-клиент (например, Antigravity или Claude Desktop):

```json
"easyeda_pro": {
  "command": "python",
  "args": [
    "C:/path/to/your/EasyEDA_MCP/easyeda_mcp.py"
  ]
}
```

### 🔌 Подключение

- MCP Server Port: `stdio`
- WebSocket Bridge Port: `8787`
- Целевой URL: `https://pro.easyeda.com/editor`

**Автоподключение:** Плагин сам сканирует порт, отдельно нажимать «Connect» не нужно. При успешном подключении в EasyEDA появится всплывающее уведомление (toast): `ATM_MCP connected`.

### 🎮 Как пользоваться

1. Запустить MCP-сервер через конфигурацию клиента ИИ.
2. Открыть EasyEDA Pro в браузере; плагин автоматически подключится по WebSocket.
3. Попросить ИИ "Расставить все компоненты на плате" или "Назначить 3D-модели моим резисторам".
4. ИИ прочитает каталог API и выполнит магию в реальном времени прямо в вашем редакторе!

**Пример вывода сервера:**

```text
[INFO] Starting EasyEDA WebSocket Server on ws://localhost:8787
[INFO] ATM_MCP WebSocket connected
[INFO] ATM_MCP event: execute-js
```

### 📦 Сборка/Запуск

- Python 3.10+
- Библиотека `websockets`
- Браузер Chrome/Edge

### ⚠️ Примечания

- Убедитесь, что EasyEDA Pro открыта и является активной вкладкой перед запуском сложных макросов для расстановки на PCB.
- Так как ИИ имеет доступ к полному недокументированному API, сложные макросы могут потребовать метода проб и ошибок в зависимости от версии EasyEDA.
