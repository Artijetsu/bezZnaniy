# Работали над проектом:
### Анафиев Тимур
### Аркаев Алексей
### Кирюханцев Александр
### Марценюк Андрей
### Молчанов Максим
========================================


### 🏰 `Clans` (Кланы)
| Поле | Тип | Описание |
|------|-----|----------|
| `id` | `INTEGER` 🏷️ | 1 |
| `name` | `TEXT` 📛 | Клан ДаНила кОбНАсеНко22822  |
| `trophies` | `INTEGER` 🏆 | 7777 |
| `max_members` | `INTEGER` 👥 | 128 |

### 👑 `Players` (Игроки)
| Поле | Тип | Описание | 
|------|-----|----------|                           
| `id` | `INTEGER` 🏷️ | 1 |
| `nickname` | `TEXT` 📛 | Rand1vu |
| `level` | `INTEGER` ⬆️ | 14 |
| `experience` | `INTEGER` ✨ | 21610 |
| `arena` | `TEXT` 🏟️ | Блинчики! |
| `clan_id` | `INTEGER` 🔗 | Trinity |       

| Поле | Тип | Описание | 
|------|-----|----------|                           
| `id` | `INTEGER` 🏷️ | 2 |
| `nickname` | `TEXT` 📛 | m0nesy |
| `level` | `INTEGER` ⬆️ | 14 |
| `experience` | `INTEGER` ✨ | 29999 |
| `arena` | `TEXT` 🏟️ | Вальхалла! |
| `clan_id` | `INTEGER` 🔗 | G2 |   

### 🃏 `Cards` (Карты)
| Поле | Тип | Описание |
|------|-----|----------|
| `id` | `INTEGER` 🏷️ | 22 |
| `name` | `TEXT` 📛 | Имya |
| `elixir_cost` | `INTEGER` ⚡ | +100500 |
| `rarity` | `TEXT` 💎 | Обычный / Редкий / ЕПИЧЕСКИ / МЕФФИЧЕСКИЙ |

### ⚔️ `Battles` (Сражения)
| Поле | Тип | Описание |
|------|-----|----------|
| `id` | `INTEGER` 🏷️ | **1** |
| `winner_id` | `INTEGER` 🥇 | **1** → `Players.id` |
| `loser_id` | `INTEGER` 😢 | **2** → `Players.id` |
| `battle_date` | `DATETIME` 📅 | **07.25.26** |
| `duration_seconds` | `INTEGER` ⏱️ | 1:34 |



#SQL Code

CREATE TABLE IF NOT EXISTS Players (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  name TEXT NOT NULL,
  level INTEGER,
  clan_id INTEGER
);
CREATE TABLE IF NOT EXISTS Clans (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  name TEXT NOT NULL,
  level INTEGER,
  max_members INTEGER NOT NULL
);
CREATE TABLE IF NOT EXISTS Battles (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  id_win INTEGER NOT NULL,
  id_lost INTEGER,
  duration_seconds INTEGER,
  data DATETIME
  
);


SELECT * FROM Players;
SELECT * FROM Clans;
SELECT * FROM Battles;
DROP TABLE Players;
DROP TABLE Clans;
DROP TABLE Battles;
