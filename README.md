# First DB App

A lightweight, zero-dependency browser application for managing customer records using the **IndexedDB API**. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no build tools, no server required.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

---

## Features

| Action | Description |
|--------|-------------|
| **Load DB** | Initializes an IndexedDB database and populates it with sample customer records |
| **Query DB** | Retrieves and displays all stored records in a formatted table |
| **Clear DB** | Deletes every record from the database |

- Real-time operation log with millisecond-precision timestamps
- Notification panel for immediate status feedback
- Responsive layout that adapts to mobile and desktop screens
- Clean neutral color palette for a distraction-free interface

## Getting Started

### Prerequisites

A modern web browser with IndexedDB support (Chrome, Firefox, Edge, Safari).

### Installation

```bash
git clone https://github.com/aadityasinhaa/First-DB.git
cd First-DB
```

Open `index.html` directly in your browser — no server or build step needed.

## Usage

1. Click **Load DB** to create the database and insert sample records
2. Click **Query DB** to view all stored customer data in a table
3. Click **Clear DB** to remove all records and reset the database

Each action is logged in the log panel with a timestamp for traceability.

## Project Structure

```
First-DB/
├── index.html    # Single-file app (HTML + CSS + JS)
├── README.md
└── .gitignore
```

The entire application lives in a single `index.html` file — HTML structure, CSS styling, and JavaScript logic are all self-contained.

## How It Works

The app uses the browser's **IndexedDB API** to persist customer data locally. The core operations:

| Operation | IndexedDB Method | Description |
|-----------|-----------------|-------------|
| `initialLoad` | `onupgradeneeded` | Creates the object store and inserts seed data |
| `queryAllRows` | `objectStore.getAll()` | Reads all records from the store |
| `removeAllRows` | `objectStore.delete()` | Iterates keys and removes each entry |

Each customer record contains:

- `userid` — Primary key
- `name` — Customer name
- `email` — Email address (unique index)
- `lastOrderDate` — Most recent order date
- `totalSalesYear` — Year-to-date sales total

## Browser Support

| Browser | Supported |
|---------|-----------|
| Chrome  | Yes |
| Firefox | Yes |
| Edge    | Yes |
| Safari  | Yes |
| IE 11   | No |

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

---

Built by [aadityasinhaa](https://github.com/aadityasinhaa)
